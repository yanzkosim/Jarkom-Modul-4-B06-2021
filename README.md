# Jarkom-Modul-4-B06-2021

## Anggota Kelompok : 
- 05111940000048 | Bagaskoro Kuncoro Ardi 
- 05111940000096 | Stefanus Albert Kosim 

## Topology

![topology](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/topology.png)

#

## VLSM - Cisco Packet Tracer

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

Subnet besar yang dibentuk memiliki NID 10.10.0.0 dengan netmask /19. 

Kemudian dihitung pembagian IP berdasarkan NID dan netmask tersebut menggunakan tree.

Dan dilakukan subnetting dengan menggunakan tree tersebut untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

![treeVLSM](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/Tree%20-%20VLSM.jpg)

Dari tree tersebut, diperoleh pembagian IP seperti berikut.

![tabelVLSM](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/tabelVLSM.png)

Selanjutnya, diatur IP untuk masing-masing interface yang ada di setiap device sesuai dengan pembagian subnet pada pohon VLSM.

Setelah IP diatur, dilakukan routing.

### FOOSHA

![routingFOOSHA1](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingFOOSHA(1).png)

![routingFOOSHA2](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingFOOSHA(2).png)

![routingFOOSHA3](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingFOOSHA(3).png)

### WATER7

![routingWATER7](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingWATER7.png)

### PUCCI

![routingPUCCI](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingPUCCI.png)

### GUANHAO

![routingGUANHAO1](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingGUANHAO(1).png)

![routingGUANHAO2](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingGUANHAO(2).png)

### ALABASTA

![routingALABAStA](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingALABASTA.png)

### OIMO

![routingOIMO](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingOIMO.png)

### SEASTONE

![routingSEASTONE](https://github.com/yanzkosim/Jarkom-Modul-4-B06-2021/blob/main/screenshot/routingVLSM/routingSEASTONE.png)

#

## CIDR - GNS3

### Perhitungan Subnet

Pada CIDR, dilakukan penggabungan subnet terluar dari topologi sebagai berikut:

#### Langkah 1

![CIDR 1]()

![CIDR 1 - tabel]()

#### Langkah 2

![CIDR 2]()

![CIDR 2 - tabel]()

#### Langkah 3

![CIDR 3]()

![CIDR 3 - tabel]()

#### Langkah 4

![CIDR 4]()

![CIDR 4 - tabel]()

#### Langkah 5

![CIDR 5]()

![CIDR 5 - tabel]()

#### Langkah 6

![CIDR 6]()

![CIDR 6 - tabel]()

#### Langkah 7

![CIDR 7]()

Pada setiap penggabungan subnet, subnet barunya akan selalu memiliki netmask yang lebih kecil dari subnet yang digabung, dimana netmask tersebut dapat dilihat di tabel tabel yang ada dibawah tiap penggabungan di topologi.

### Pembagian IP

Setelah penggabungan subnet selesai dilakukan, selanjutnya ialah mengatur pembagian IP. Pembagian IP dilakukan dengan menggunakan tree sebagai berikut

![Tree CIDR]()

Pembagian menggunakan tree ini dilakukan dengan melihat wildcard dari tabel subnet yang ada di modul. Misalnya NID kiri adalah 10.10.0.0 /18, maka NID kanan adalah NID kiri + wildcard netmask 18 yaitu 0.0.63.255, lalu angka bukan 0 paling kiri ditambah 1 sehingga NID kanan adalah 10.10.64.255 /X. X adalah subnet dari pembagian di topologi

Dari tree yang dibuat, maka dapat dituliskan tabel pembagian IP dari subnet A sebagai berikut 

![Tabel Pembagian IP]()

Untuk subnet B keatas, dapat langsung dilihat dari pembagian di Tree karena yang dibutuhkan adalah NID dan subnetmask saja.

### Topologi

Selanjutnya adalah membuat topologi di GNS3

![Topologi]()

Lalu isi static address setiap node pada GNS3 berdasarkan pembagian IP yang telah dibuat. Untuk pembagian ip di subnet, router paling atas diisi IP berupa NID + 1, selanjutnya diikuti dengan pola +1, dengan router sebagai fokus utama. eth0 pada Foosha diisi dengan dhcp karena terhubung dengan NAT. 

```
# Foosha
    auto eth0
    iface eth0 inet dhcp

    auto eth1
    iface eth1 inet static
        address 10.10.128.1
        netmask 255.255.252.0

    auto eth2
    iface eth2 inet static
        address 10.10.64.1
        netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
        address 10.10.132.1
        netmask 255.255.255.252

    auto eth4
    iface eth4 inet static
        address 10.11.64.1
        netmask 255.255.255.252

# Water7
    auto eth0
    iface eth0 inet static
        address 10.10.64.2
        netmask 255.255.255.252

    auto eth1
    iface eth1 inet static
        address 10.10.16.1
        netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
        address 10.10.32.1
        netmask 255.255.252.0

# Pucci
    auto eth0
    iface eth0 inet static
        address 10.10.16.2
        netmask 255.255.255.252

    auto eth1
    iface eth1 inet static
        address 10.10.8.1
        netmask 255.255.255.128

    auto eth2
    iface eth2 inet static
        address 10.10.0.1
        netmask 255.255.248.0

# Guanhao
    auto eth0
    iface eth0 inet static
        address 10.11.64.2
        netmask 255.255.255.252

    auto eth1
    iface eth1 inet static
        address 10.11.36.1
        netmask 255.255.252.0

    auto eth2
    iface eth2 inet static
        address 10.11.32.1
        netmask 255.255.254.0

    auto eth3
    iface eth3 inet static
        address 10.11.16.1
        netmask 255.255.255.252

# Alabasta
    auto eth0
    iface eth0 inet static
        address 10.11.32.2
        netmask 255.255.254.0

    auto eth1
    iface eth1 inet static
        address 10.11.34.1
        netmask 255.255.255.240

# Oimo
    auto eth0
    iface eth0 inet static
        address 10.11.16.2
        netmask 255.255.255.252

    auto eth1
    iface eth1 inet static
        address 10.11.8.1
        netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
        address 10.11.4.1
        netmask 255.255.255.0

# Seastone
    auto eth0
    iface eth0 inet static
        address 10.11.4.2
        netmask 255.255.255.0

    auto eth1
    iface eth1 inet static
        address 10.11.0.1
        netmask 255.255.252.0
```

Gateway pada tiap end-device adalah IP router yang memiliki nilai NID + 1.

### Routing

Routing di CIDR lebih mudah daripada routing di VLSM karena NID yang digunakan bisa diambil dari NID gabungan. Dalam topologi yang dibuat ini, routing yang digunakan adalah sebagai berikut


FOOSHA
```
route add -net 10.10.0.0 netmask 255.255.192.0 gw 10.10.64.2
route add -net 10.11.0.0 netmask 255.255.192.0 gw 10.11.64.2
```
PUCCI
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.10.16.1
```
WATER7
```
route add -net 10.10.0.0 netmask 255.255.240.0 gw 10.10.16.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.10.64.1
```
GUANHAO
```
route add -net 10.11.0.0 netmask 255.255.240.0 gw 10.11.16.2
route add -net 10.11.34.0 netmask 255.255.255.240 gw 10.11.32.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.11.64.1
```
ALABASTA
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.11.32.1
```
OIMO
```
route add -net 10.11.0.0 netmask 255.255.252.0 gw 10.11.4.2
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.11.16.1
```
SEASTONE
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.11.4.1
```

Keterangan:

- Routing di Foosha menggunakan NID Subnet E2 dan D1
- Routing di Water7 menggunakan NID Subnet B1 dan default routing yang mengarah ke Foosha
- Routing di Guanhao menggunakan NID Subnet C2, A11 dan default routing
- Routing di Oimo menggunakan NID Subnet A14 dan default routing
- Routing di router ujung hanya menggunakan default routing yaitu 0.0.0.0/0 yang mengarah ke router atasnya

### Testing

Sebelum melakukan testing, tambahkan command berikut ke tiap node :
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
```
dan command berikut ke router Foosha:
```
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 10.10.0.0/15
```

iptables ini digunakan agar tiap-tiap node bisa mengakses internet. -s atau source address nya adalah NID dan netmask dari subnet terbesar yaitu G1 `10.10.0.0/15`.

Testing yang dilakukan adalah melakukan ping dari server Fukurou ke `Router Pucci`, `Client Courtyard`, `Server Doriki`, dan `my.its.ac.id`.

1. Pucci

![Testing Pucci]()

2. Courtyard

![Testing Courtyard]()

3. Doriki

![Testing Doriki]()

4. my.its.ac.id

![Testing my.its.ac.id]()