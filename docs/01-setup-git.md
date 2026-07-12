# 01 — Setup Git

Panduan setup Git untuk repo sandbox ini.

## Prasyarat

- Git terinstall (`git --version`)
- Akun GitHub (akun kamu: **fiidev**)
- GitHub CLI (`gh`) — opsional tapi disarankan

## Clone Repo

```bash
git clone https://github.com/fiidev/git-sandbox.git
cd git-sandbox
```

## Konfigurasi Git (sekali saja)

Pastikan identitas sudah benar:

```bash
git config --global user.name "Nama Kamu"
git config --global user.email "email@example.com"
```

Cek:

```bash
git config user.name
git config user.email
```

## Login GitHub CLI

```bash
gh auth login
gh auth status
```

## Perintah Git Dasar

| Perintah | Fungsi |
|----------|--------|
| `git status` | Lihat file yang berubah |
| `git add .` | Stage semua perubahan |
| `git commit -m "pesan"` | Simpan snapshot |
| `git push` | Upload ke GitHub |
| `git pull` | Download perubahan terbaru |
| `git log --oneline` | Riwayat commit |

## Commit Pertama (latihan)

```bash
echo "# catatan belajar" >> catatan.md
git add catatan.md
git commit -m "docs: tambah catatan belajar"
git push origin main
```

> **Tip:** Di repo sandbox ini, lebih baik latihan lewat branch + PR daripada push langsung ke `main`.

## Langkah Selanjutnya

→ [02 — Issue dan Branch](02-issue-dan-branch.md)
