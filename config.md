# Topologi Jaringan dengan Routing RIP

## Detail Proyek
- **Nama**: Sadat Ardiansyah
- **NIM**: 20210801180
- **Mata Kuliah**: Jaringan Komputer Lanjut (Jarkom Lanjut UTS)
- **Universitas**: Universitas Esa Unggul

## Penjelasan Komponen

### 1. Subnet

- **192.168.20.0/24**: Subnet untuk laptop yang terhubung ke **Router 1 (KJ)**.
- **192.168.21.0/24**: Subnet untuk laptop yang terhubung ke **Router 2 (CR)**.
- **192.168.23.0/24**: Subnet untuk laptop yang terhubung ke **Router 3 (KHI)**.
- **10.10.10.0/24**: Subnet untuk koneksi antara **Router 1 (KJ)** dan **Router 2 (CR)**.
- **15.15.15.0/24**: Subnet untuk koneksi antara **Router 1 (KJ)** dan **Router 3 (KHI)**.
- **25.25.25.0/24**: Subnet untuk koneksi antara **Router 2 (CR)** dan **Router 3 (KHI)**.

### 2. Interface

- **Router 1 (KJ)**
  - **Ether 2**: 192.168.20.1/24 — Terhubung ke laptop pada subnet 192.168.20.0/24.
  - **Ether 3**: 10.10.10.2/24 — Terhubung ke Router 2 (CR) pada subnet 10.10.10.0/24.
  - **Ether 3**: 15.15.15.2/24 — Terhubung ke Router 3 (KHI) pada subnet 15.15.15.0/24.

- **Router 2 (CR)**
  - **Ether 2**: 192.168.21.1/24 — Terhubung ke laptop pada subnet 192.168.21.0/24.
  - **Ether 3**: 10.10.10.1/24 — Terhubung ke Router 1 (KJ) pada subnet 10.10.10.0/24.
  - **Ether 4**: 25.25.25.2/24 — Terhubung ke Router 3 (KHI) pada subnet 25.25.25.0/24.

- **Router 3 (KHI)**
  - **Ether 2**: 192.168.23.1/24 — Terhubung ke laptop pada subnet 192.168.23.0/24.
  - **Ether 3**: 15.15.15.1/24 — Terhubung ke Router 1 (KJ) pada subnet 15.15.15.0/24.
  - **Ether 4**: 25.25.25.1/24 — Terhubung ke Router 2 (CR) pada subnet 25.25.25.0/24.

### 3. Jaringan Antar-Router

- **Jaringan 10.10.10.0/24**: Menghubungkan **Router 1 (KJ)** dengan **Router 2 (CR)**.
- **Jaringan 15.15.15.0/24**: Menghubungkan **Router 1 (KJ)** dengan **Router 3 (KHI)**.
- **Jaringan 25.25.25.0/24**: Menghubungkan **Router 2 (CR)** dengan **Router 3 (KHI)**.