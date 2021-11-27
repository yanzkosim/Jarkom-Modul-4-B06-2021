# Jarkom-Modul-4-B06-2021

## Anggota Kelompok : 
- 05111940000048 | Bagaskoro Kuncoro Ardi 
- 05111940000096 | Stefanus Albert Kosim 

## Topology

![topology](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/topology.png)

#

## VLSM

Dari topology, ditentukan subnet-subnet yang terdapat pada topology. Sehingga diperoleh subnet-subnet berikut.

![VLSM](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/Topologi%20-%20VLSM.png)

Kemudian dientukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan dilakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.

| Subnet | Jumlah IP | Netmask |
| :----: | --------: | :-----: |
| A1 | 101 | /25 |
| A2 | 2021 | /21 |
| A3 | 2 | /30 |
| A4 | 701 | /22 |
| A5 | 2 | /30 |
| A6 | 1001 | /22 |
| A7 | 2 | /30 |
| A8 | 2 | /30 |
| A9 | 521 | /22 |
| A10 | 502 | /23 |
| A11 | 13 | /28 |
| A12 | 2 | /30 |
| A13 |	252 | /24 |
| A14 | 721 | /22 |
| A15 |2 | /30 |
| **Total** | **5845** | **/19** |

Kemudian

Subnet besar yang dibentuk memiliki NID 10.10.0.0 dengan netmask /19. 

Kemudian dihitung pembagian IP berdasarkan NID dan netmask tersebut menggunakan tree.

Dan dilakukan subnetting dengan menggunakan tree tersebut untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

![treeVLSM](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/Tree%20-%20VLSM.jpg)

Dari tree tersebut, diperoleh pembagian IP seperti berikut.

![tabelVLSM](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/tabelVLSM.png)

#

## CIDR
