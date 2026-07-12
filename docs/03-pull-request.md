# 03 — Pull Request

Belajar buka PR, review, dan merge ke `main`.

## Apa itu Pull Request?

PR = permintaan untuk menggabungkan perubahan branch kamu ke `main`. Tim (atau kamu sendiri) bisa review sebelum merge.

## Buat PR

### Via Web

1. Push branch ke GitHub
2. Klik banner **Compare & pull request**
3. Isi template:
   - **Summary:** apa yang berubah
   - **Issue terkait:** `Closes #1`
   - **Test plan:** langkah verifikasi

### Via CLI

```bash
gh pr create \
  --title "feat: tambah fungsi multiply" \
  --body "$(cat <<'EOF'
## Summary
Menambahkan fungsi `multiply(a, b)` di calculator.

Closes #1

## Test plan
- [x] `pytest tests/test_calculator.py::test_multiply -v`
EOF
)"
```

## CI (Continuous Integration)

Setiap PR ke `main` otomatis menjalankan pytest via GitHub Actions.

- ✅ Hijau = test lulus, aman merge
- ❌ Merah = ada test gagal, perbaiki dulu

Cek status di tab **Checks** pada PR.

## Review PR

Meskipun solo, latihan review tetap berguna:

1. Buka tab **Files changed**
2. Klik **Review changes**
3. Pilih **Comment**, **Approve**, atau **Request changes**

## Merge

Setelah CI hijau:

1. Klik **Squash and merge** (disarankan)
2. Edit commit message jika perlu
3. Confirm merge
4. Hapus branch: **Delete branch**

Issue dengan `Closes #N` otomatis tertutup.

## Perintah CLI Berguna

```bash
gh pr list                    # daftar PR
gh pr view 1                  # detail PR
gh pr checks 1                # status CI
gh pr merge 1 --squash        # merge PR
```

## Langkah Selanjutnya

→ Mulai latihan di [docs/latihan/](latihan/)
