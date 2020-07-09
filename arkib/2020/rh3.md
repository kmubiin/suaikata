### Rumus gunaan daftar kerapu

Berikut adalah senarai rumus gunaan bagi daftar kata kerap
unik (kerapu).

‘~’ ke ‘-’  
`=SUBSTITUTE(B2,"~","-")`

nyah ‘.’ akhir  
`=IF(RIGHT(C2,2)=" .",SUBSTITUTE(C2," .",""),C2)`

‘ ,’ ke ‘;’  
`=SUBSTITUTE(D2," ,",";")`

‘ ;’ ke ‘;’  
`=SUBSTITUTE(E2," ;",";")`

‘ .’ ke ‘’  
`=SUBSTITUTE(F2," .","")`

‘(iv), iv)’ ke ‘4 ’  
`=SUBSTITUTE(SUBSTITUTE(G2,"(iv)","4 "),"iv)","4 ")`

‘(iii), iii)’ ke ‘3 ’  
`=SUBSTITUTE(SUBSTITUTE(H2,"(iii)","3 "),"iii)","3 ")`

‘(ii), ii)’ ke ‘2 ’  
`=SUBSTITUTE(SUBSTITUTE(I2,"(ii)","2 "),"ii)","2 ")`

‘(i), I)’ ke ‘1 ’  
`=SUBSTITUTE(SUBSTITUTE(J2,"(i)","1 "),"i)","1 ")`

'1), 2)’ ke ‘1 ‘ ‘2 ‘  
`=SUBSTITUTE(SUBSTITUTE(K2,"1)","1 "),"2)","2 ")`

buang semua lebihan aksara kosong  
`=TRIM(L2)`

Melalui semua rumus gunaan di atas, hasil yang didapati
adalah lajur baharu "terjemah" dalam daftar kerapu.

Daftar kerapu menggunakan perisian komputer LibreOffice Calc
untuk menjalankan semua rumus gunaan di atas. Boleh mencuba
perisian lain dengan rumus yang sama atau sedikit berbeza.

laman kembali: [arkib][0]

  [0]: ../index.md
