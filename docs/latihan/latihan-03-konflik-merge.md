# Latihan 03 — Resolve Konflik Merge

**Tujuan:** Belajar menangani merge conflict — situasi umum saat dua branch mengedit baris yang sama.

## Skenario

Dua branch mengedit `src/calculator.py` di tempat yang sama. Saat merge, Git tidak bisa otomatis memilih versi mana — kamu harus resolve manual.

## Checklist

- [ ] Pastikan `main` up to date: `git checkout main && git pull`
- [ ] Buat branch A: `git checkout -b feat/konflik-a`
- [ ] Edit baris komentar di `src/calculator.py`, commit, push
- [ ] Kembali ke `main`, buat branch B: `git checkout main && git checkout -b feat/konflik-b`
- [ ] Edit baris **yang sama** dengan isi berbeda, commit, push
- [ ] Merge branch A dulu ke `main` (via PR)
- [ ] Coba merge branch B ke `main` (via PR) — konflik muncul
- [ ] Resolve konflik lokal atau via GitHub web editor
- [ ] Commit resolve, push, merge PR

## Langkah Resolve Lokal

```bash
git checkout main
git pull origin main
git checkout feat/konflik-b
git merge main
# Git menandai konflik di file
# Edit file, hapus marker <<<<<<, ======, >>>>>>
git add src/calculator.py
git commit -m "fix: resolve merge conflict di calculator"
git push
```

## Marker Konflik

```
<<<<<<< HEAD
# versi branch kamu
=======
# versi dari main
>>>>>>> main
```

Hapus marker dan pilih/gabungkan isi yang benar.

## Verifikasi

- PR branch B berhasil merge tanpa marker konflik
- `src/calculator.py` berisi versi final yang kamu pilih

## Tips

- Konflik bukan error — itu normal di tim
- Selalu `git pull` sebelum mulai branch baru
- PR kecil = konflik lebih jarang
