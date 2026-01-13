```markdown
<p align="center">
  <a href="https://onnobot-agent.com/latest/">
    <img src="assets/onnobot-agent-banner.png" alt="onnobot-agent.com" style="height: 7em" />
  </a>
</p>

<p align="center">
<a href="https://onnobot-agent.com/latest/"><img src="https://img.shields.io/badge/Docs-green?style=for-the-badge&logo=materialformkdocs&logoColor=white" alt="Docs"></a>
<a href="https://join.slack.com/t/onnobot-bench/shared_invite/zt-36pj9bu5s-o3_yXPZbaH2wVnxnss1EkQ"><img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" alt="Slack"></a>
<a href="https://arxiv.org/abs/2405.15793"><img src="https://img.shields.io/badge/arxiv-2405.15793-red?style=for-the-badge&logo=arxiv&logoColor=white&labelColor=black" alt="arxiv 2405.15793"></a>
</p>

onnobot-agent memungkinkan model bahasa pilihan Anda (mis. GPT-4o atau Claude Sonnet 4) untuk secara otonom menggunakan tools guna
[memperbaiki isu di repositori GitHub nyata](https://onnobot-agent.com/latest/usage/hello_world),
[mencari kerentanan keamanan siber](https://enigma-agent.com/), atau
[melakukan tugas kustom apa pun](https://onnobot-agent.com/latest/usage/coding_challenges).

* ✅ **State of the art** pada onnobot-bench untuk proyek open-source
* ✅ **Fleksibel & dapat digeneralisasi**: Memberi agen LM kebebasan yang luas
* ✅ **Terkonfigurasi & terdokumentasi**: Dikendalikan oleh file `yaml`
* ✅ **Dirancang untuk riset**: Sederhana & mudah dimodifikasi

onnobot-agent dibuat dan dipelihara oleh peneliti dari Princeton University dan Stanford University.

## 📣 Berita

* July 24: [Mini-onnobot-Agent](https://github.com/onnobot-agent/mini-onnobot-agent) mencapai 65% pada onnobot-bench dalam 100 baris Python!
* May 2: [onnobot-agent-LM-32b](https://github.com/onnobot-bench/onnobot-smith) mencapai open-weights SOTA pada onnobot-bench
* Feb 28: [onnobot-agent 1.0 + Claude 3.7 adalah SoTA pada onnobot-bench full](https://x.com/KLieret/status/1895487966409298067)

## 🚀 Mulai cepat!

👉 Coba onnobot-agent di browser Anda: [![Open in GitHub Codespaces](https://img.shields.io/badge/Open_in_GitHub_Codespaces-gray?logo=github)](https://codespaces.new/onnobot-agent/onnobot-agent) ([lebih lanjut](https://onnobot-agent.com/latest/installation/codespaces/))

Baca dokumentasi kami untuk info lebih lanjut:

* [Instalasi](https://onnobot-agent.com/latest/installation/source/)
* [Hello world lewat command line](https://onnobot-agent.com/latest/usage/hello_world/)
* [Benchmarking di onnobot-bench](https://onnobot-agent.com/latest/usage/batch_mode/)
* [FAQ](https://onnobot-agent.com/latest/faq/)

## onnobot-agent untuk keamanan ofensif (EnIGMA)

[onnobot-agent: EnIGMA][enigma] adalah mode untuk menyelesaikan tantangan keamanan ofensif (capture the flag).
EnIGMA mencapai hasil terbaik pada beberapa benchmark keamanan siber (lihat [leaderboard](https://enigma-agent.com/#results)).
Silakan gunakan [onnobot-agent 0.7](https://github.com/onnobot-agent/onnobot-agent/tree/v0.7) jika Anda memakai EnIGMA sambil menunggu pembaruan untuk versi 1.0.

[enigma]: https://enigma-agent.com

Di samping itu, Anda mungkin tertarik pada proyek terkait kami:

<div align="center">
  <a href="https://github.com/onnobot-agent/mini-onnobot-agent"><img src="docs/assets/mini_logo_text_below.svg" alt="Mini-onnobot-Agent" height="120px"></a>
   &nbsp;&nbsp;
  <a href="https://github.com/onnobot-agent/onnobot-ReX"><img src="docs/assets/onnobotrex_logo_text_below.svg" alt="onnobot-ReX" height="120px"></a>
   &nbsp;&nbsp;
  <a href="https://github.com/onnobot-bench/onnobot-bench"><img src="docs/assets/onnobotbench_logo_text_below.svg" alt="onnobot-bench" height="120px"></a>
  &nbsp;&nbsp;
  <a href="https://github.com/onnobot-bench/onnobot-smith"><img src="docs/assets/onnobotsmith_logo_text_below.svg" alt="onnobot-smith" height="120px"></a>
  &nbsp;&nbsp;
  <a href="https://github.com/onnobot-bench/sb-cli"><img src="docs/assets/sbcli_logo_text_below.svg" alt="sb-cli" height="120px"></a>
</div>

## Kontribusi

Jika Anda ingin berkontribusi, kami menerima [issues](https://github.com/onnobot-agent/onnobot-agent/issues) dan [pull requests](https://github.com/onnobot-agent/onnobot-agent/pulls)! Untuk perubahan besar, mohon diskusikan lewat issue terlebih dahulu.

## Sitasi & kontak

onnobot-agent adalah proyek akademik yang dimulai di Princeton oleh John Yang*, Carlos E. Jimenez*, Alexander Wettig, Kilian Lieret, Shunyu Yao, Karthik Narasimhan, dan Ofir Press.
Kontak: [John Yang](https://john-b-yang.github.io/), [Carlos E. Jimenez](http://www.carlosejimenez.com/), [Kilian Lieret](https://www.lieret.net/) (Email: johnby@stanford.edu, carlosej@cs.princeton.edu, kl5675@princeton.edu).

Jika proyek ini berguna untuk Anda, pertimbangkan untuk menyitirnya:

<details>
<summary> Sitasi onnobot-agent</summary>

```bibtex
@inproceedings{yang2024onnobotagent,
  title={{onnobot}-agent: Agent-Computer Interfaces Enable Automated Software Engineering},
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

[![Pytest](https://github.com/onnobot-agent/onnobot-agent/actions/workflows/pytest.yaml/badge.svg)](https://github.com/onnobot-agent/onnobot-agent/actions/workflows/pytest.yaml)
[![build-docs](https://github.com/onnobot-agent/onnobot-agent/actions/workflows/build-docs.yaml/badge.svg)](https://github.com/onnobot-agent/onnobot-agent/actions/workflows/build-docs.yaml)
[![codecov](https://codecov.io/gh/onnobot-agent/onnobot-agent/graph/badge.svg?token=18XAVDK365)](https://codecov.io/gh/onnobot-agent/onnobot-agent)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/onnobot-agent/onnobot-agent/main.svg)](https://results.pre-commit.ci/latest/github/onnobot-agent/onnobot-agent/main)

</div>
```
