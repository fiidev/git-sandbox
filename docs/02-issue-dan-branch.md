# 02 — Issue dan Branch

Belajar alur: buat issue dulu, lalu kerjakan di branch terpisah.

## Kenapa Issue Dulu?

Issue = catatan pekerjaan. Manfaatnya:

- Ada deskripsi jelas apa yang dikerjakan
- Bisa di-link ke PR (`Closes #1`)
- Riwayat kerja terdokumentasi

## Buat Issue

### Via Web

1. Buka https://github.com/fiidev/git-sandbox/issues
2. Klik **New issue**
3. Pilih template → isi → submit

### Via CLI

```bash
gh issue create \
  --title "feat: tambah fungsi multiply" \
  --body "Implementasi fungsi multiply di src/calculator.py" \
  --label "good first issue,enhancement"
```

## Buat Branch dari Issue

### Via Web

Di halaman issue, klik **Create a branch** (sidebar kanan).

### Via CLI

```bash
git checkout main
git pull origin main
git checkout -b feat/multiply
```

## Konvensi Nama Branch

```
feat/multiply          ← fitur baru
fix/divide-by-zero     ← perbaikan bug
docs/readme-update     ← dokumentasi
```

Format: `{tipe}/{deskripsi-singkat}`

## Kerjakan & Commit

```bash
# edit src/calculator.py
git add src/calculator.py
git commit -m "feat: tambah fungsi multiply"
git push -u origin feat/multiply
```

## Assign Issue ke Diri Sendiri

Via web: buka issue → **Assignees** → pilih akun kamu.

Via CLI:

```bash
gh issue edit 1 --add-assignee @me
```

## Langkah Selanjutnya

→ [03 — Pull Request](03-pull-request.md)
