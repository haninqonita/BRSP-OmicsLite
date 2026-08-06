# Laporan Interpretasi Hasil
## Simulasi Molecular Docking TNF dan Gibberellin a5

Molecular docking adalah teknik komputasi yang digunakan dalam in silico drug delivery systems untuk memprediksi bagaimana ligan berinteraksi dengan reseptor target. Teknik ini mensimulasikan orientasi pengikatan dan menghitung binding affinity untuk mengoptimalkan pemuatan obat, mekanisme pelepasan, dan stabilitas pembawa. Dalam simulasi ini, ligan dan target yang digunakan diambil dari hasil network pharmacology yang telah dilakukan sebelumnya.

TNF dipilih sebagai protein target karena memiliki koneksi terbanyak dengan target lain sehingga menunjukkan nilai Degree terbaik. TNF dalam malaria memang diyakini meningkatkan pembunuhan parasit melalui aktivasi makrofag dan pelepasan sitokin. Namun, saat eritrosit yang terinfeksi pecah jumlah TNF akan sangat berlebihan akibat adanya rangsangan sel makrofag. Dalam kondisi yang berlebihan, mediator ini dapat merusak jaringan tubuh pasien itu sendiri. Maka dari itu TNF perlu untuk dikendalikan dengan senyawa anti-TNF.

![This is an alt text.](/spesifikasi_ligan-target.png "This is a sample image.")

Langkah awal yang dilakukan adalah melakukan studi literatur mengenai mekanisme inhibisi TNF dalam malaria. Selanjutnya mencari PDB ID target melalui Uniprot dan Protein Data Bank (RCSB PDB). Mengingat kode yang ditawarkan UniProt terkait TNF sangat bervariasi, penulis menargetkan 2AZ5 dari kode UniProt ID P01375 dengan resolusi 2.10 Å. Meskipun resolusinya dapat dikatakan kurang optimal karena lebih dari 2 Å, tetapi 2AZ5 masih menjadi PDB ID yang paling sering digunakan dalam literatur yang melibatkan TNF dalam malaria maupun TNF yang menyangkut penyakit lain. Sementara itu, kode SMILES senyawa yang dipilih yaitu Gibberellin a5 dicari melalui PubChem. 

Simulasi ini murni dilakukan menggunakan SwissDock (Docking with AutoDock Vina) tanpa bantuan aplikasi tambahan. Langkah awalnya yaitu memasukkan kode SMILES Gibberellin a5 dan mempreparasinya. Setelah itu, memasukkan PDB ID 2AZ5 dengan chain A dan B, dimana gabungan chain ini sering digunakan dalam penelitian molecular docking sebelumnya. Penulis juga tidak ingin mempertahankan heteroatom sehingga opsi “None” dipilih. Kemudian untuk search box pada Seach Space penulis menyesuaikan dengan pocket center yang paling ideal seperti yang telah diperoleh dari PrankWeb yaitu -10, 68, 19. Dan untuk sampling exhaustivity, penulis menggunakan setelan default yaitu 4.

![This is an alt text.](/prank_web.png "This is a sample image.")

![This is an alt text.](/visualisasi_docking.png "This is a sample image.")

![This is an alt text.](/binding_affinity.png "This is a sample image.")

Simulasi ini menghasilkan 20 model korformasi dengan Calculated affinity terendah sebesar -3.731. Angka yang cukup baik untuk menggambarkan potensi kuatnya ikatan yang terbentuk antara Gibberelin a5 dengan target. Rendahnya angka ini juga menjadi alasan mengapa Gibberalin a5 dipilih menjadi senyawa kandidat terbaik. Penulis telah melakukan simulasi pada kelima senyawa yang terlihat sama signifikannya pada hasil network pharmacology sebelumnya. Hasilnya, Gibberellin a5 menunjukkan binding affinity terbaik. Meskipun begitu, nilai ini tidak bisa dijadikan parameter mutlak yang menetukan efektif atau tidaknya suatu senyawa. Binding affinity hanya menunjukkan seberapa kuat molekul atau obat dapat menempel pada protein targetnya. Sementara itu, keefektifan juga dipengaruhi oleh kemampuan senyawa dalam memicu efek biologis (efficacy) serta sifat farmakokinetiknya di dalam tubuh.

![This is an alt text.](/model_1.png "This is a sample image.")

Hasil simulasi juga menunjukkan bahwa model 1 yang dihasilkan memiliki cukup banyak ikatan. Ikatan yang terbentuk meliputi ikatan hidrogen yang ditunjukkan oleh garis putus biru dan ikatan hidrofik yang ditunjukkan oleh garis putus abu-abu. Ikatan-ikatan ini dapat menurunkan nilai Calculated affinity sehingga meningkatkan kekuatan ikatan ligan dengan target.

Ketika dibandingkan dengan kurkumin, senyawa yang sangat banyak diteliti sebagai anti-TNF, Gibberellin a5 menunjukkan nilai binding affinity yang lebih tinggi. Kurkumin memiliki nilai binding affinity sebesar -3.966, memiliki selisih 235 dengan Gibberellin a5. Perbedaan yang tidak signifikan ini mengindikasikan bahwa senyawa Gibberellin a5 kemungkinan dapat memiliki pengaruh terhadap TNF meskipun ikatannya tidak sekuat kurkumin. Hal ini juga menunjukkan bahwa Gibberellin a5 dapat menjadi salah satu kandidat yang bisa mengontrol inflamasi pada malaria dengan cara mengikat TNF bebas sebagai mediator utama sitokin pro-inflamasi yang dilepaskan sel makrofag.
