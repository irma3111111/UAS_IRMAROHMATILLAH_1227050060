Ujian Akhir Semester

Mata Kuliah : Dasar Pemrograman
Nama : Irma Rohmatillah
NIM : 1227050060
Jurusan :Teknik Informatika UIN Sunan Gunung Djati Bandung
 
Matriks merupakan kumpulan-kumpulan bilangan yang disusun secara baris (vertikal) dan kolom (horizontal) bisa disebut juga array dua dimensi (multi-dimensional). Transpose Matriks adalah memperoleh sebuah matriks dengan cara menukar baris menjadi kolom dan kolom menjadi baris dari sebuah matriks

#include <iostream>
using namespace std;

int main() {
 int arr[100][100], transpose[100][100], baris, kolom;
 
 cout << "baris: "; cin >> baris;
 cout << "kolom: "; cin >> kolom;
 
 for(int i=0; i<baris; i++){
  for(int j=0; j<kolom; j++){
   cout << "arr ke["<<i<<j<<"]: "; cin >> arr[i][j];
  }
 }
 
 cout << endl;
 
 for(int i=0; i<baris; i++){
  for(int j=0; j<kolom; j++){
   cout << arr[i][j] << " ";
   if(j == kolom - 1);
  }
  cout << endl;
 }
 
 cout << endl;
 

 for(int i=0; i<baris; i++){
  for(int j=0; j<kolom; j++){
   transpose[j][i] = arr[i][j];
  }
 }
 
 for(int i=0; i<kolom; i++){
  for(int j=0; j<baris; j++){
   cout << transpose[i][j] << " ";
   if(j == baris - 1);
  }
  cout << endl;
 }
}
OUTPUT

Matriks (2 x 3)
4 5 6
7 8 3
Transpos matriks
4 7
5 8
6 3

