```markdown
<p align="center">
  <a href="https://swe-agent.com/latest/">
    <img src="assets/swe-agent-banner.png" alt="swe-agent.com" style="height: 7em" />
  </a>
</p>

<p align="center">
<a href="https://swe-agent.com/latest/"><img src="https://img.shields.io/badge/Docs-green?style=for-the-badge&logo=materialformkdocs&logoColor=white" alt="Docs"></a>
<a href="https://join.slack.com/t/swe-bench/shared_invite/zt-36pj9bu5s-o3_yXPZbaH2wVnxnss1EkQ"><img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" alt="Slack"></a>
<a href="https://arxiv.org/abs/2405.15793"><img src="https://img.shields.io/badge/arxiv-2405.15793-red?style=for-the-badge&logo=arxiv&logoColor=white&labelColor=black" alt="arxiv 2405.15793"></a>
</p>

SWE-agent memungkinkan model bahasa pilihan Anda (mis. GPT-4o atau Claude Sonnet 4) untuk secara otonom menggunakan tools guna
[memperbaiki isu di repositori GitHub nyata](https://swe-agent.com/latest/usage/hello_world),
[mencari kerentanan keamanan siber](https://enigma-agent.com/), atau
[melakukan tugas kustom apa pun](https://swe-agent.com/latest/usage/coding_challenges).

* ✅ **State of the art** pada SWE-bench untuk proyek open-source
* ✅ **Fleksibel & dapat digeneralisasi**: Memberi agen LM kebebasan yang luas
* ✅ **Terkonfigurasi & terdokumentasi**: Dikendalikan oleh file `yaml`
* ✅ **Dirancang untuk riset**: Sederhana & mudah dimodifikasi

SWE-agent dibuat dan dipelihara oleh peneliti dari Princeton University dan Stanford University.

## 📣 Berita

* July 24: [Mini-SWE-Agent](https://github.com/SWE-agent/mini-SWE-agent) mencapai 65% pada SWE-bench dalam 100 baris Python!
* May 2: [SWE-agent-LM-32b](https://github.com/SWE-bench/SWE-smith) mencapai open-weights SOTA pada SWE-bench
* Feb 28: [SWE-agent 1.0 + Claude 3.7 adalah SoTA pada SWE-bench full](https://x.com/KLieret/status/1895487966409298067)

## 🚀 Mulai cepat!

👉 Coba SWE-agent di browser Anda: [![Open in GitHub Codespaces](https://img.shields.io/badge/Open_in_GitHub_Codespaces-gray?logo=github)](https://codespaces.new/SWE-agent/SWE-agent) ([lebih lanjut](https://swe-agent.com/latest/installation/codespaces/))

Baca dokumentasi kami untuk info lebih lanjut:

* [Instalasi](https://swe-agent.com/latest/installation/source/)
* [Hello world lewat command line](https://swe-agent.com/latest/usage/hello_world/)
* [Benchmarking di SWE-bench](https://swe-agent.com/latest/usage/batch_mode/)
* [FAQ](https://swe-agent.com/latest/faq/)

## SWE-agent untuk keamanan ofensif (EnIGMA)

[SWE-agent: EnIGMA][enigma] adalah mode untuk menyelesaikan tantangan keamanan ofensif (capture the flag).
EnIGMA mencapai hasil terbaik pada beberapa benchmark keamanan siber (lihat [leaderboard](https://enigma-agent.com/#results)).
Silakan gunakan [SWE-agent 0.7](https://github.com/SWE-agent/SWE-agent/tree/v0.7) jika Anda memakai EnIGMA sambil menunggu pembaruan untuk versi 1.0.

[enigma]: https://enigma-agent.com

Di samping itu, Anda mungkin tertarik pada proyek terkait kami:

<div align="center">
  <a href="https://github.com/SWE-agent/mini-SWE-agent"><img src="docs/assets/mini_logo_text_below.svg" alt="Mini-SWE-Agent" height="120px"></a>
   &nbsp;&nbsp;
  <a href="https://github.com/SWE-agent/SWE-ReX"><img src="docs/assets/swerex_logo_text_below.svg" alt="SWE-ReX" height="120px"></a>
   &nbsp;&nbsp;
  <a href="https://github.com/SWE-bench/SWE-bench"><img src="docs/assets/swebench_logo_text_below.svg" alt="SWE-bench" height="120px"></a>
  &nbsp;&nbsp;
  <a href="https://github.com/SWE-bench/SWE-smith"><img src="docs/assets/swesmith_logo_text_below.svg" alt="SWE-smith" height="120px"></a>
  &nbsp;&nbsp;
  <a href="https://github.com/SWE-bench/sb-cli"><img src="docs/assets/sbcli_logo_text_below.svg" alt="sb-cli" height="120px"></a>
</div>

## Kontribusi

Jika Anda ingin berkontribusi, kami menerima [issues](https://github.com/SWE-agent/SWE-agent/issues) dan [pull requests](https://github.com/SWE-agent/SWE-agent/pulls)! Untuk perubahan besar, mohon diskusikan lewat issue terlebih dahulu.

## Sitasi & kontak

SWE-agent adalah proyek akademik yang dimulai di Princeton oleh John Yang*, Carlos E. Jimenez*, Alexander Wettig, Kilian Lieret, Shunyu Yao, Karthik Narasimhan, dan Ofir Press.
Kontak: [John Yang](https://john-b-yang.github.io/), [Carlos E. Jimenez](http://www.carlosejimenez.com/), [Kilian Lieret](https://www.lieret.net/) (Email: johnby@stanford.edu, carlosej@cs.princeton.edu, kl5675@princeton.edu).

Jika proyek ini berguna untuk Anda, pertimbangkan untuk menyitirnya:

<details>
<summary> Sitasi SWE-agent</summary>

```bibtex
@inproceedings{yang2024sweagent,
  title={{SWE}-agent: Agent-Computer Interfaces Enable Automated Software Engineering},
  author={John Yang and Carlos E Jimenez and Alexander Wettig and Kilian Lieret and Shunyu Yao and Karthik R Narasimhan and Ofir Press},
  booktitle={The Thirty-eighth Annual Conference on Neural Information Processing Systems},
  year={2024},
  url={https://arxiv.org/abs/2405.15793}
}
```
</details>

## Lisensi

MIT. Lihat `LICENSE`.

<div align="center">

[![Pytest](https://github.com/SWE-agent/SWE-agent/actions/workflows/pytest.yaml/badge.svg)](https://github.com/SWE-agent/SWE-agent/actions/workflows/pytest.yaml)
[![build-docs](https://github.com/SWE-agent/SWE-agent/actions/workflows/build-docs.yaml/badge.svg)](https://github.com/SWE-agent/SWE-agent/actions/workflows/build-docs.yaml)
[![codecov](https://codecov.io/gh/SWE-agent/SWE-agent/graph/badge.svg?token=18XAVDK365)](https://codecov.io/gh/SWE-agent/SWE-agent)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/SWE-agent/SWE-agent/main.svg)](https://results.pre-commit.ci/latest/github/SWE-agent/SWE-agent/main)

</div>
```
