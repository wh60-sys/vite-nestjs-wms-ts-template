# Enterprise WMS Monorepo Template | Vite + NestJS + TypeScript
### vite-nestjs-wms-ts-template
"Template monorepo siap pakai untuk membangun Warehouse Management System (WMS) tingkat internasional. Sudah terkonfigurasi untuk FEFO/FIFO Enforcement, RBAC Tingkat Lanjut, Traceability Batch, dan integrasi GPS/Barcode Verification."

---

➡️ 1. Fitur Utama (Value Proposition)

Arsitektur: Monorepo (Frontend dan Backend terpisah dalam satu workspace).

Frontend: React 18, TypeScript, Vite.

Backend: NestJS, TypeScript (Struktur Modular Siap-Audit).

Database: PostgreSQL (Melalui Docker Compose).

Caching/Queue: Redis (Melalui Docker Compose).

Keamanan Inti: Struktur awal untuk JSON Web Token (JWT) dan RBAC Guard.

Kepatuhan: Struktur untuk alur kerja QC (Karantina) dan FEFO Enforcement.

---

➡️ 2. Persyaratan Sistem & Instalasi

Persyaratan: Node.js (v18+), Docker, GitHub Codespaces (Disarankan).

Langkah Awal (Setup Database):

docker-compose up -d (Menjalankan Postgres & Redis).

Langkah Awal (Instalasi Modul):

npm install -g @nestjs/cli

cd backend && npm install

cd ../frontend && npm install

---

➡️ 3. Panduan Pengembangan Cepat

Menjalankan Backend (BE): cd backend && npm run start:dev

Menjalankan Frontend (FE): cd frontend && npm run dev

Migrasi Database (Contoh): Perintah ORM yang digunakan (misalnya, npm run migration:run).

---

➡️ 4. Struktur Folder Kunci (Sangat Penting)

/
├── .devcontainer/         # Konfigurasi Codespaces/Dev Container
├── backend/               # Proyek NestJS (BE)
│   ├── src/modules/       # Auth, Inventory, QC, Compliance Modules
│   └── ormconfig.ts       # Konfigurasi DB
├── frontend/              # Proyek Vite/React (FE)
│   ├── src/api/           # Axios Service Layer
│   └── src/modules/       # Login, WMS, Compliance Pages
└── docker-compose.yml     # Database & Redis Configuration

---





