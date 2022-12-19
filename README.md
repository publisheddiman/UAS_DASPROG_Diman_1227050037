## Ujian Akhir Semester 

		<br>Mata Kuliah 	: Dasar Pemograman
		<br> Nama		: Diman Fathurohman
		<br>NIM		        : 1227050037
		<br>Jurusan		: [Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum

		Matriks adalah sekumpulan bilangan yang disusun berdasarkan baris dan kolom, serta ditempatkan di dalam tanda kurung. Nah, tanda kurungnya ini bisa berupa kurung biasa “( )” atau kurung siku “[ ]”, ya. Suatu matriks diberi nama dengan huruf kapital, seperti A, B, C, dan seterusnya.

		Transpose matriks adalah matriks baru yang diperoleh dengan cara menukar elemen-elemen baris menjadi elemen kolom atau sebaliknya.

## Source Code

		#include<iostream>
		using namespace std;


		int main()
		{
		int m, n;

		cout << "UAS DASAR PEMOGRAMAN"<<endl;
		cout << "===="<<endl;
		cout << "Nama : Diman Fathurohman"<<endl;
		cout << "NIM  : 1227050037"<<endl;
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

		//buat pada array 2 dimensi angka-angka, menampilkan bilangan yang tidak habis dibagi 3, 5, dan 7  
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
		cout << "Nilai yang tidak bisa dibagi 3, 5, 7 yaitu :";
		for (int i = 0; i < m; i++)
		{
			for (int j = 0; j < n; j++)
			{
				if (matriks[i][j]%3!=0 && matriks[i][j]%5!=0 && matriks[i][j]%7!=0)
				{
					cout << " " << matriks[i][j];
					cek = false;
				}
			}
		}
		if (cek)
		{
			cout << " Nilai yang anda input bisa dibagi 3, 5 dan 7" <<endl;
		}
		return 0;

		}

## Output

		UAS DASAR PEMOGRAMAN
		====
		Nama : Diman Fathurohman
		NIM  : 1227050037
		======================================


		No.1 Mengubah baris jadi kolom dan kolom jadi baris (transpose)
		===============================================================
		Masukkan jumlah baris matriks: 2
		Masukkan jumlah kolom matriks: 2
		Masukkan Nilai-Nilai Matriks
		Baris ke 1, Kolom ke 1 : 1
		Baris ke 1, Kolom ke 2 : 2
		Baris ke 2, Kolom ke 1 : 3
		Baris ke 2, Kolom ke 2 : 4
		Hasil dari matriks yang diinputkan :
		1       2
		3       4

		Hasil Transpose Matriks:
		1       3
		2       4

		No.2 Menampilkan bilangan yang habis dibagi 3, 5 dan 7
		===============================================================
		Masukkan jumlah baris matriks: 2
		Masukkan jumlah kolom matriks: 2
		Masukkan Nilai-Nilai
		(1,1) : 1
		(1,2) : 2
		(2,1) : 3
		(2,2) : 4

		Nilai yang tidak bisa dibagi 3, 5, 7 yaitu : 1 2 4
		--------------------------------
		Process exited after 20.39 seconds with return value 0
		Press any key to continue . . .
