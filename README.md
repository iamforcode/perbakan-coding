#include <stdio.h>

int main() {
    int id, harga = 0, jumlah_tiket= 0, total_harga = 0;
    int uang_bayar, kembalian;
    char ulang;
    int jumlah_item = 0;
    char nama[50], judul[50];

    // Menyimpan informasi item yang dibeli
    int item_dipilih[100];
    int harga_item[100];

    // Menampilkan daftar judul film dan harga tiket
    printf("Selamat datang di Bioskop kami!\n");
    printf("----------------------------------------------------------------------------------\n");
    printf("|  ID  |       Judul Film                     |  Harga Tiket    | Jam Tayang     |\n");
    printf("----------------------------------------------------------------------------------\n");
    printf("|  1   |  GODZILLA VS KONG                    | Rp 75.000       | 09:00am        |\n");
    printf("|  2   |  A QUIET PLACE                       | Rp 150.000      | 10:45am        |\n");
    printf("|  3   |  CRUELLA                             | Rp 150.000      | 18:00pm        |\n");
    printf("|  4   |  GHOSTBUSTERS: AFTERLIFE             | Rp 100.000      | 19:00pm        |\n");
    printf("|  5   |  TENET                               | Rp 80.000       | 16:30pm        |\n");
    printf("|  6   | The Marvel                           | Rp 90.000       | 17:00pm        |\n");
    printf("|  7   | Nanti Kita Cerita Tentang Hari Ini   | Rp 65.000       | 18:30pm        |\n");
    printf("|  8   | Jalan Jauh Jangan Lupa Pulang        | Rp 75.000       | 19:20pm        |\n");
    printf("|  9   | Killers of the Flower Moon           | Rp 85.000       | 15:00pm        |\n");
    printf("|  10  | Five Nights at Freddy’s              | Rp 60.000       | 20:00pm        |\n");
    printf("----------------------------------------------------------------------------------\n\n");

    printf("Masukkan nama Anda: ");
    scanf(" %[^\n]", nama);

    do {
         int valid_id = 0;
        while (!valid_id) {
            printf("Masukkan ID Tiket yang ingin anda beli: ");
            scanf("%d", &id);


        switch (id) {
            case 1: harga = 75000;
                printf("Anda memilih Tiket Film GODZILLA VS KONG dengan harga Rp %d\n", harga);
                break;
            case 2: harga = 150000;
                printf("Anda memilih Tiket Film A QUIET PLACE dengan harga Rp %d\n", harga);
                break;
            case 3: harga = 150000;
                printf("Anda memilih Tiket Film CRUELLA dengan harga Rp %d\n", harga);
                break;
            case 4: harga = 100000;
                printf("Anda memilih Tiket Film GHOSTBUSTERS: AFTERLIFE dengan harga Rp %d\n", harga);
                break;
            case 5: harga = 200000;
                printf("Anda memilih Tiket Film TENET dengan harga Rp %d\n", harga);
                break;
            case 6: harga = 400000;
                printf("Anda memilih Tiket The Marvel dengan harga Rp %d\n", harga);
                break;
            case 7: harga = 100000;
                printf("Anda memilih Tiket Nanti Kita Cerita Tentang Hari Ini dengan harga Rp %d\n", harga);
                break;
            case 8: harga = 900000;
                printf("Anda memilih Tiket Jalan Jauh Jangan Lupa Pulang dengan harga Rp %d\n", harga);
                break;
            case 9: harga = 120000;
                printf("Anda memilih Tiket Killers of the Flower Moont dengan harga Rp %d\n", harga);
                break;
            case 10: harga = 200000;
                printf("Anda memilih Tiket  Five Nights at Freddy’s  dengan harga Rp %d\n", harga);
                break;
            default:
                printf("ID tiket tidak valid. Silakan pilih ID yang benar (1-10).\n");
                continue;
        }

        printf("Jumlah Tiket Yang Ingin Dibeli: ");
        scanf("%d", &jumlah_tiket);

        // Simpan item yang dipilih
        item_dipilih[jumlah_item] = id;
        harga_item[jumlah_item] = harga * jumlah_tiket;
        total_harga += harga_item[jumlah_item];
        jumlah_item++;

        printf("\nMau beli tiket lagi? (y/t): ");
        scanf(" %c", &ulang);

    }
     while (ulang == 'y' || ulang == 'Y');

    printf("\nNama: %s\n", nama);
    printf("Total harga yang harus dibayar: Rp %d\n", total_harga);
    printf("Masukkan uang pembayaran: ");
    scanf("%d", &uang_bayar);

    if (uang_bayar >= total_harga) {
        kembalian = uang_bayar - total_harga;
        printf("Kembalian: Rp %d\n", kembalian);
    } else {
        printf("Uang pembayaran tidak cukup.\n");
        printf("masukkan uang pembayaran: ");
        scanf("%d", &uang_bayar)
    }

