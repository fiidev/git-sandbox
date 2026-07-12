# Git Sandbox

Repo **public** untuk latihan workflow GitHub — buat issue, branch, pull request, merge, dan lihat CI jalan.

Ini bukan project production. Eksperimen sepuasnya di sini.

## Quick Start

```bash
git clone https://github.com/fiidev/git-sandbox.git
cd git-sandbox
git checkout -b feat/nama-fitur
# edit file, lalu:
git add .
git commit -m "feat: deskripsi perubahan"
git push -u origin feat/nama-fitur
gh pr create
```

## Alur Kerja

```
Issue → Branch → Commit → Push → Pull Request → CI → Merge
```

Baca panduan lengkap di [CONTRIBUTING.md](CONTRIBUTING.md).

## Latihan

| Latihan | File |
|---------|------|
| Issue pertama | [docs/latihan/latihan-01-issue-pertama.md](docs/latihan/latihan-01-issue-pertama.md) |
| PR pertama | [docs/latihan/latihan-02-pr-pertama.md](docs/latihan/latihan-02-pr-pertama.md) |
| Resolve konflik merge | [docs/latihan/latihan-03-konflik-merge.md](docs/latihan/latihan-03-konflik-merge.md) |

## Panduan Git

- [01 — Setup Git](docs/01-setup-git.md)
- [02 — Issue dan Branch](docs/02-issue-dan-branch.md)
- [03 — Pull Request](docs/03-pull-request.md)

## Kode Latihan

Kalkulator sederhana di `src/calculator.py` — beberapa fungsi belum diimplementasi. Lihat [Issues](https://github.com/fiidev/git-sandbox/issues) untuk target PR.

```bash
pip install pytest
pytest tests/
```

## CI

Setiap PR ke `main` menjalankan pytest otomatis via GitHub Actions.
