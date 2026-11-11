name: CI-CD Kampus

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Mengambil Kode
        uses: actions/checkout@v4

      - name: Menjalankan Build
        run: echo "Build aplikasi berhasil"

      - name: Menjalankan Testing
        run: echo "Testing aplikasi berhasil"

      - name: Deployment
        run: echo "Aplikasi siap di-deploy"
