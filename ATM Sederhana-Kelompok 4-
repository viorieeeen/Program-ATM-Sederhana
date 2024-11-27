#include <iostream>
#include <string>
using namespace std;

class ATM {
private:
    string pin;
    double saldo;

public:
    // Constructor untuk menginisialisasi PIN dan saldo awal
    ATM(string p, double s) {
        pin = p;
        saldo = s;
    }

    // Method untuk memverifikasi PIN
    bool verifikasiPin(string inputPin) {
        return pin == inputPin;
    }

    // Method untuk cek saldo
    void cekSaldo() {
        cout << "Saldo Anda saat ini: Rp " << saldo << endl;
    }

    // Method untuk setor tunai
    void setorTunai(double jumlah) {
        if (jumlah > 0) {
            saldo += jumlah;
            cout << "Setoran berhasil! Saldo Anda saat ini: Rp " << saldo << endl;
        } else {
            cout << "Jumlah setor tidak valid!" << endl;
        }
    }

    // Method untuk tarik tunai
    void tarikTunai(double jumlah) {
        if (jumlah <= saldo) {
            saldo -= jumlah;
            cout << "Tarik tunai berhasil! Saldo Anda saat ini: Rp " << saldo << endl;
        } else {
            cout << "Saldo tidak cukup!" << endl;
        }
    }
};

int main() {
    string pinInput;
    int pilihan;
    double jumlah;

    // Membuat objek ATM dengan PIN '1234' dan saldo awal 500000
    ATM atm("1234", 500000);

    cout << "Selamat datang di ATM Sederhana\n";
    cout << "Masukkan PIN Anda: ";
    cin >> pinInput;

    // Memverifikasi PIN
    if (!atm.verifikasiPin(pinInput)) {
        cout << "PIN salah! Akses ditolak.\n";
        return 0;
    }

    do {
        // Menampilkan menu
        cout << "\nMenu ATM:\n";
        cout << "1. Cek Saldo\n";
        cout << "2. Setor Tunai\n";
        cout << "3. Tarik Tunai\n";
        cout << "4. Keluar\n";
        cout << "Pilih menu (1/2/3/4): ";
        cin >> pilihan;

        switch (pilihan) {
            case 1:
                atm.cekSaldo();
                break;

            case 2:
                cout << "Masukkan jumlah setor: Rp ";
                cin >> jumlah;
                atm.setorTunai(jumlah);
                break;

            case 3:
                cout << "Masukkan jumlah tarik tunai: Rp ";
                cin >> jumlah;
                atm.tarikTunai(jumlah);
                break;

            case 4:
                cout << "Terima kasih, sampai jumpa!\n";
                break;

            default:
                cout << "Pilihan tidak valid!\n";
                break;
        }
    } while (pilihan != 4);

    return 0;
}
