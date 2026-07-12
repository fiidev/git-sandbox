# Latihan 02 — PR Pertama

**Tujuan:** Selesaikan starter issue #1 (`feat: tambah fungsi multiply`) lewat branch + PR + merge.

## Checklist

- [ ] Baca issue #1 di GitHub
- [ ] Buat branch: `git checkout -b feat/multiply`
- [ ] Implementasi `multiply(a, b)` di `src/calculator.py`
- [ ] Pastikan test lulus: `pytest tests/test_calculator.py::test_multiply -v`
- [ ] Commit: `git commit -m "feat: tambah fungsi multiply"`
- [ ] Push: `git push -u origin feat/multiply`
- [ ] Buat PR dengan body berisi `Closes #1`
- [ ] Tunggu CI hijau
- [ ] Squash and merge
- [ ] Hapus branch
- [ ] Pastikan issue #1 otomatis tertutup

## Implementasi Hint

```python
def multiply(a, b):
    return a * b
```

## Buat PR via CLI

```bash
gh pr create \
  --title "feat: tambah fungsi multiply" \
  --body "Closes #1

## Summary
Menambahkan fungsi multiply ke calculator.

## Test plan
- [x] pytest tests/test_calculator.py::test_multiply -v"
```

## Verifikasi

- PR merged ke `main`
- Issue #1 status: **Closed**
- `main` branch punya fungsi `multiply`

## Selanjutnya

→ [Latihan 03 — Konflik Merge](latihan-03-konflik-merge.md)
