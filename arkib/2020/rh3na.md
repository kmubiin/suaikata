### Daftar kerapu ada hasil #N/A

Semasa mengusahakan daftar kata kerap unik (kerapu), rumus
gunaan memberi jumlah baris unik yang salah. Hal ini kerana
rumus tersebut bagi baris tertentu ada hasil `#N/A`.

Apabila diteliti, ada tiga tempat hasil ini dijumpai, iaitu
baris 7471, 10761, 10765. Kesemua baris ini mengandungi
hasil tersebut dan dikira oleh rumus sebagai `0`. Hasil
`#N/A` berpunca daripada aksara `~` dalam terjemahan asal.

Untuk memahami hal ini, lihat di baris asal 7471.

|      | B        | C                   |
| ---- | -------- | ------------------- |
| 7470 | moral    |                     |
| 7471 | moral... | =MATCH(B7471,B:B,0) |

> Sel B7471:  
> moral , morality BER~ = have high moral standard .  

Pada asalnya, sel B7471 ada aksara `~`, sel C7471 akan
memberi hasil `#N/A`. Apabila aksara `~` diganti dengan
aksara `-` di sel yang sama, hasil akan berubah menjadi
`7471` yakni padanan tepat pertama ada di baris sel itu.
Ini adalah benar.

Aksara `=` pula didapati tidak menjejaskan hasil di sel
C7471 dan tidak menjadi masalah.

Kesimpulannya, ada aksara yang boleh menjejaskan hasil
kiraan menggunakan rumus dalam helaian rebak; aksara `~`
diganti dengan `-` yang menyamai fungsi aksara asal.

laman kembali: [arkib][0]

  [0]: ../pokok.md
