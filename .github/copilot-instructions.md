# Panduan untuk Copilot / Agen AI pada SWE-agent (ringkas)

Tujuan: memberi agen pemrograman AI konteks minimal dan konkret yang diperlukan untuk membuat perubahan yang aman dan berguna atau menjalankan proyek secara lokal.

Ringkasan singkat (1 baris tiap poin)
- Titik masuk: `sweagent` (console script -> `sweagent.run.run:main`). Gunakan `sweagent --help` untuk melihat subperintah seperti `run`, `run-batch`, `run-shell`, `run-replay`.
- Konfigurasi default: `config/default.yaml` — CLI menerima `--config` (bisa dipakai berulang) untuk memuat file YAML tambahan.
- Pengujian: gunakan `pytest` (konfigurasi ada di `pyproject.toml`); CI menjalankan workflow di `.github/workflows/pytest.yaml`.
- Kunci & `.env`: kunci model / GitHub disediakan lewat variabel lingkungan atau `.env` (lihat `docs/installation/keys.md`).

Arsitektur — bagian penting (baca sebelum mengubah perilaku)
- Orkestrasi CLI: `sweagent.run.*` (lihat `sweagent/run/run.py`, `run_single.py`, `run_shell.py`). File-file ini memuat konfigurasi dan menginisialisasi `SWEEnv` + Agent.
- Loop Agent: `sweagent.agent.*` — `Agent.forward()` mengelola prompting, parsing, dan eksekusi aksi. History processors berada di `sweagent/agent/history_processors.py` dan memengaruhi bagaimana history dikompres sebelum dikirim ke model.
- Lingkungan eksekusi: `sweagent.environment.swe_env.SWEEnv` membungkus `swerex` Deployment; perintah dijalankan di dalam container/shell session.
- Tools & parser: implementasi tools dan helper parsing ada di `sweagent/tools/*` (lihat `tools/parsing.py`). Pilihan parser (function-calling vs. `thought_action`) dikonfigurasi di YAML.
- Inspector / UI: inspector kecil berbasis Flask + SocketIO ada di `sweagent/inspector/`.

Alur kerja pengembang & perintah penting
- Setup pengembangan lokal: `pip install -e '.[dev]'` (CI menggunakan extras yang sama).
- Menjalankan satu issue/instance secara lokal (contoh):
  `sweagent run --config config/default.yaml --agent.model.name "gpt-4o" --agent.model.api_key "$OPENAI_API_KEY"`
- Mode semi-interaktif (berguna untuk debugging):
  `sweagent run-shell --repo /path/to/repo --config config/exotic/default_shell.yaml`
- Batch / benchmark: `sweagent run-batch --config config/benchmarks/250522_anthropic_filemap_simple_review.yaml --num_workers=20` (lihat contoh di `config/benchmarks/`).
- Pengujian: `pytest` (gunakan marker `-m "not slow"` atau `-m ctf` untuk tes EnIGMA/CTF).
- Pre-commit & linting: repo memakai `pre-commit` dan pengaturan `ruff` di `pyproject.toml`. Gaya proyek: gunakan tanda kutip ganda, lebar baris 120.

Konvensi proyek & hal yang perlu diperhatikan (konkret)
- Config-first: perilaku dikendalikan oleh file YAML (`config/default.yaml` dan preset lainnya). Selalu periksa file konfigurasi yang digunakan; lebih baik menambah/memperbarui config daripada meng-hardcode konstanta.
- Mode parser: default menggunakan function-calling; **jika model Anda tidak mendukung function-calling**, gunakan `agent.tools.parse_function.type: thought_action` (lihat `docs/installation/keys.md` dan `docs/reference/parsers.md`).
- History processors: beberapa processor (mis. `cache_control`) mengubah format pesan — nonaktifkan atau hapus jika model tidak kompatibel (lihat `sweagent/agent/history_processors.py`).
- Model lokal: untuk model lokal dengan endpoint OpenAI-compatible, tetapkan `agent.model.name` sebagai `provider/model` dan perhatikan pengaturan pelacakan biaya (`per_instance_cost_limit`, `max_input_tokens`). Lihat `docs/installation/keys.md`.
- CI: tes berjalan pada Python 3.11 dan 3.12 (`.github/workflows/pytest.yaml`) dan CI menginstal dependensi lewat `uv pip install`; tiru pemasangan `pip install -e '.[dev]'` secara lokal sebelum menjalankan tes.

Tempat melihat contoh (file yang berguna)
- Ikhtisar arsitektur: `docs/background/architecture.md` ✅
- Konfigurasi & contoh: `config/default.yaml`, `config/*.yaml` (`benchmarks/`, `demo/`, `exotic/`)
- CLI: `sweagent/run/run.py`, `run_single.py`, `run_shell.py`
- Internal Agent: `sweagent/agent/agents.py`, `sweagent/agent/history_processors.py`, `sweagent/agent/models.py`
- Tools & parsing: `sweagent/tools/parsing.py`, `sweagent/tools/*`
- Tes contoh pola: `tests/test_run_*`, `tests/test_parsing.py`, `tests/test_agent.py`

Tugas awal yang baik untuk agen AI
- Perbaikan bug kecil: jalankan tes, buat skrip reproduksi lokal, tambahkan unit test kecil di `tests/` yang menangkap regresi, lalu lakukan perbaikan dan jalankan `pytest`.
- Perubahan konfigurasi: lebih baik tambah file YAML di `config/` dan perbarui dokumentasi; sertakan contoh CLI satu baris di header file config (lihat `config/benchmarks/*.yaml`).
- Tools & parser: tambahkan unit test untuk keluaran parser di `tests/test_parsing.py`; pastikan format tetap konsisten (JSON atau blok triple-backtick sesuai `parse_function.type`).

Keamanan & tata cara PR
- Selalu jalankan `pytest` secara lokal; pastikan perubahan tidak memecah matrix CI (3.11 & 3.12). Gunakan dev extras yang sama seperti CI.
- Tambahkan/ubah tes untuk perubahan perilaku, perbarui `docs/` bila perilaku terlihat pengguna, dan sebutkan file config yang relevan di deskripsi PR.

Jika ada yang tidak jelas
- Tanyakan: konfigurasi mana (daftar lengkap `--config`) dan versi Python (3.11 vs 3.12) yang diinginkan maintainer untuk reproduksi isu.

---
Silakan tinjau terjemahan ini; beri tahu bagian mana yang ingin Anda perluas atau jika Anda mau saya tambahkan contoh prompt (canned prompts) singkat untuk agen AI.