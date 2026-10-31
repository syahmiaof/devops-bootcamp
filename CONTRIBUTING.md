# Panduan Sumbangan (Contributing Guidelines)

Terima kasih kerana berminat menyumbang kepada repositori latihan **DevOps Bootcamp 2026**. Dokumen ini menggariskan tatacara sumbangan, etika git, dan amalan terbaik keselamatan.

---

## 🌿 Aliran Kerja Git & Percabangan (Branching Strategy)

1. **Cawangan Utama (`main`)**: Cawangan stabil yang hanya menerima kod teruji melalui Pull Request (PR).
2. **Cawangan Ciri / Modul**: Bina cawangan baharu bagi setiap modul atau latihan:
   ```bash
   git checkout -b feature/nama-modul
   # contoh: git checkout -b docker-exercise-2
   ```

---

## 💬 Format Mesej Komit (Conventional Commits)

Gunakan mesej komit yang jelas dan deskriptif berasaskan piawaian industri:
- `feat:` Penambahan modul, skrip, atau konfigurasi baharu
- `fix:` Pembetulan ralat skrip, sintaks, atau tetapan persekitaran
- `docs:` Pengemaskinian dokumentasi, nota pembelajaran, atau README
- `chore:` Penyelenggaraan rutin (cth: `.gitignore`, pembaharuan lesen)

Contoh:
```bash
git commit -m "feat(docker): add multi-stage Dockerfile configuration"
git commit -m "docs(aws): document IAM least-privilege exercise notes"
```

---

## 🔒 Kebersihan Keselamatan & Data Sensitif

1. **JANGAN sesekali memasukkan rahsia**: Kunci API, token peribadi (PAT), fail `.env`, kata laluan, atau fail log (`*.log`) dilarang sama sekali dikomit ke dalam repositori.
2. Gunakan template `.env.example` dengan nilai contoh atau bertopeng (*masked*).
3. Sentiasa semak `git status` dan `git diff` sebelum melakukan `git commit`.

---

## 🚀 Prosedur Pull Request (PR)

1. Tolak cawangan anda ke remote:
   ```bash
   git push origin feature/nama-modul
   ```
2. Buka Pull Request ke cawangan `main`.
3. Nyatakan objektif perubahan, senarai arahan yang telah diuji, dan sertakan tangkapan skrin atau log output jika berkenaan.
4. Pastikan semakan CI automatik (syntax/lint) lulus sepenuhnya sebelum penggabungan (*merge*).
