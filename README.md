# Manajemen Proses 

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/52671c43-a805-4e65-a7c3-9fd8476d5b05)  

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/37ca8741-3c3a-4809-a29e-1596ffe53843)  

1. Login sebagai studentOS dan lihat status proses, perhatikan kolom keluaran ps –au sebagai 
berikut :

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/2c88529d-76dd-4bf7-8b29-96c1bb3ff729)  

a. Sebutkan nama-nama proses yang bukan root  
   jawab : Proses yang bukan root adalah proses yang menggunakan user azza  
   
b. Tulis PID dan COMMAND dari proses yang paling banyak menggunakan CPU time
    jawab : proses yang paling  banyak menggunakan CPU adalah proses dengan  PID 1477 dan COMMAND /usr/libexec.   
    
c. Sebutkan buyut proses dan PID dari proses tersebut .  
    Jawab : Parent proses dari PID 1477 berada di direktori /usr/  
    
d. Sebutkan beberapa proses daemon 
    Jawab : Umumnya proses daemon pada UNIX berakhiran d, tapi karena diatas tidak ada yang berakhiran d berarti tidak ada  
    
e. Pada prompt login lakukan hal-hal sebagai berikut : 
$ csh 
$ who 
$ bash 
$ ls 
$ sh 
$ ps

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/a2327f66-0bee-428b-be52-e715f39bb8b6)

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/e29bd37c-ae41-4e88-8f28-23634a04818b)  

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/0adf7c1d-4af7-4233-a491-0be59c0db972)  

![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/78b25a2d-64df-4913-8e04-686f48425c1d)  

Sebutkan PID yang paling besar dan kemudian buat urut-urutan proses sampai ke PPID =1. 
Lakukan ^d atau exit atau logout sampai kembali muncul login: prompt

3. Modifikasi program prog.sh sebagai berikut :
   ![image](https://github.com/Azzadlyh/SO-Praktikum6-ManajemenProses/assets/126213404/447b197c-7af1-44bb-9d88-f014c1175c22)  

$ vi prog.sh 
#!/bin/sh 
trap “echo Hello Goodbye ; exit 0 “ 1 2 3 15 
echo “Program berjalan …” 
while : 
do 
echo “X” 
sleep 20 
done
Jalankan program tersebut sebagai background. Coba lakukan kil dengan nomor sinyal 1, 2, 3 
dan 15 pada nomor PID proses tersebut. Apakah proses berhenti atau tetap berjalan ? Nomor 
sinyal berapa yang digunakan untuk menghentikan proses diatas ?

5. Modifikasi program 
myjob.sh. Buatlah trap sedemikian rupa, sehingga bila proses tersebut dihentikan (kil), otomatis 
file berkas akan terhapus. 
$ vi myjob.sh 
#!/bin/sh 
trap ______________________________ 
i=1 
while : 
do 
 find / -print > berkas 
 sort berkas –o hasil 
 echo “Proses selesai pada „date‟” >> proses.log 
sleep 60 
done 
$ kill –15 [Nomor PID] 
$ ls -l
