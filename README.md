Ujian Akhir Semester

Mata Kuliah : Dasar Pemrograman
Nama : Irma Rohmatillah
NIM : 1227050060
Jurusan :Teknik Informatika UIN Sunan Gunung Djati Bandung

Deskripsi Umum

Pada program kali ini dibuat untuk memenuhi Ujian Akhir Semester(UAS) mata kuliah Dasar Pemrograman, pada program ini terdapat 2 soal yaitu:
1. Mengubah baris jadi kolom dan kolom jadi baris (transpose)
Pada program ini kita akan mengubah nilai baris yang diinputkan menjadi kolom pada hasil dan mengubah nilai kolom yang diinputkan menjadi baris pada hasil, ini disebut juga transpose
2. Menampilkan bilangan yang habis dibagi 3, 5 dan 7
Pada program ini kita akan mengecek bilangan yang diinputkan apakah bisa dibagi dengan bilangan 3, 5, 7 atau tidak

Source Code

#include
using namespace std;


int main()
{
int m, n;

cout << "UAS"<<endl;
cout << "===="<<endl;
cout << "Nama : Irma Rohmatillah"<<endl;
cout << "NIM  : 1227050060"<<endl;
cout << "======================================"<<endl<<endl<<endl;

cout << "No.1 Mengubah baris jadi kolom dan kolom jadi baris (transpose)" << endl;
cout << "==============================================================="<<endl;
cout << "Masukkan jumlah baris matriks: ";
cin >> m;
cout << "Masukkan jumlah kolom matriks: ";
cin >> n;

int matriks[m][n], transpose[n][m];

cout << "Masukkan Nilai-Nilai Matriks\n";
for (int i = 0; i < m; i++)
{
	for (int j = 0; j < n; j++)
	{
		cout <<"Baris ke "<<i+1<<", Kolom ke "<<j+1<<" : ";
		cin  >> matriks[i][j];
	}
}

cout << "Hasil dari matriks yang diinputkan :\n";
for (int i = 0; i < m; i++)
{
	for (int j = 0; j < n; j++)
	{
		cout << matriks[i][j] << "\t";
	}
	cout << endl;
}
cout << endl;

for (int i = 0; i < m; i++)
{
	for (int j = 0; j < n; j++)
	{
  		transpose[j][i] = matriks[i][j];
	}
}

cout << "Hasil Transpose Matriks: \n";
for (int i = 0; i < n; i++)
{
	for (int j = 0; j < m; j++)
	{
		cout << transpose[i][j] << "\t";
	}
	cout << endl;
}
cout <<endl;

//buat pada array 2 dimensi angka-angka, menampilkan bilangan yang habis dibagi 3, 5, dan 7  
cout << "No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7" << endl;
cout << "==============================================================="<<endl;
cout << "Masukkan jumlah baris matriks: ";
cin >> m;
cout << "Masukkan jumlah kolom matriks: ";
cin >> n;

cout << "Masukkan Nilai-Nilai\n";
for (int i = 0; i < m; i++)
{
	for (int j = 0; j < n; j++)
	{
		cout <<"("<<i+1<<","<<j+1<<") : ";
		cin  >> matriks[i][j];
	}
}
cout << endl;

bool cek = true;
cout << "Nilai yang bisa dibagi 3, 5, 7 yaitu :";
for (int i = 0; i < m; i++)
{
	for (int j = 0; j < n; j++)
	{
		if (matriks[i][j]%3==0 && matriks[i][j]%5==0 && matriks[i][j]%7==0)
		{
			cout << " " << matriks[i][j];
			cout << endl;
			cek = false;
		}
	}
}
if (cek)
{
	cout << " Nilai yang anda input tidak bisa dibagi 3, 5 dan 7" <<endl;
}
return 0;

}

Output

UAS
====
Nama : Irma Rohmatillah
NIM : 1227050060
======================================


No.1 Mengubah baris jadi kolom dan kolom jadi baris (transpose)
===============================================================
Masukkan jumlah baris matriks: 2
Masukkan jumlah kolom matriks: 2
Masukkan Nilai-Nilai Matriks
Baris ke 1, Kolom ke 1 : 2
Baris ke 1, Kolom ke 2 : 3
Baris ke 2, Kolom ke 1 : 4
Baris ke 2, Kolom ke 2 : 5
Hasil dari matriks yang diinputkan :
2 3
4 5


Hasil Transpose Matriks:
2 4
3 5


No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7
===============================================================
Masukkan jumlah baris matriks: 2
Masukkan jumlah kolom matriks: 2
Masukkan Nilai-Nilai
(1,1) : 1
(1,2) : 2
(2,1) : 105
(2,2) : 210


Nilai yang bisa dibagi 3, 5, 7 yaitu :
105
210
