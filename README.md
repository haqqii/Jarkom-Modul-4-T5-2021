# Jarkom-Modul-4-T5-2021
Oleh :

1. Shavica Ihya Q A L (05311940000013)
2. Gerry Putra Fresnando (05311940000031)
3. Mohammad Ibadul Haqqi (05311940000037)

---
VLSM

![Screenshot 2021-11-27 105423](https://user-images.githubusercontent.com/73151522/143667259-8ef05a11-1683-4fe8-bb16-76f44b95449a.jpg)

![Frame 1 (1)](https://user-images.githubusercontent.com/73151522/143667216-522d7229-6c8c-431a-b248-64cf8eb02861.png)

Tabel 

![image](https://user-images.githubusercontent.com/61973814/143667180-0df8b2f2-bf62-4fc3-9429-b4360974484e.png)

Setelah membuat tree, maka menentukan semua ip yang ada di dalam tree tersebut dengan cara melihat tabel pada diatas. Maka didapatkan jumlah semua IP dan ditentekan sebagai berikut :

![Screenshot 2021-11-27 105528](https://user-images.githubusercontent.com/73151522/143667285-94668a15-24db-47b5-9a30-cd1543005d6d.jpg)
![Screenshot 2021-11-27 105545](https://user-images.githubusercontent.com/73151522/143667288-bef2ef7c-404f-4128-809a-173c98469791.jpg)
![Screenshot 2021-11-27 105602](https://user-images.githubusercontent.com/73151522/143667291-34c2a326-cd83-4578-99b6-1d211b65540b.jpg)

Setelah ditentukan Ip nya maka kita masukkan ke dalam PC, dan Router nya. Seperti contoh pada berikut :

![image](https://user-images.githubusercontent.com/61973814/143666288-c79b6191-5e10-4ac6-9a50-a57e94775e2a.png)

![image](https://user-images.githubusercontent.com/61973814/143668378-774b1ff3-e7c7-42f9-bfb9-85b764feb49c.png)

Pada gambar diatas termasuk pada circle A3 yang berarti ip pada router nya adalah `10.44.0.129`. dan `/25` menandakan subnetnya `255.255.255.128`. Sedangkan pada Client nya di setting dengan ip address `10.44.0.129` dan subnetnya sama seperti rourternya yaitu `255.255.255.128`

![image](https://user-images.githubusercontent.com/61973814/143667875-12357ad3-f839-4a80-af81-560efb2f5521.png)

setelah dimasukkan ip dan subnet pada router dan clientnya maka kita coba testing, jika sudah succesfull maka berhasil


ROUTING

PUCCI

![image](https://user-images.githubusercontent.com/61973814/143666318-28d78537-834e-43ac-ab52-165dbd86a4db.png)


WATER7

![image](https://user-images.githubusercontent.com/61973814/143666330-985cc6a1-dd82-4886-a1af-3ba2fcf9d43f.png)


FOOSHA

![image](https://user-images.githubusercontent.com/61973814/143666351-31125531-c6a1-4e91-a3fb-c5b6e8c8bf53.png)
![image](https://user-images.githubusercontent.com/61973814/143666367-da10718f-079e-4b1e-aa97-b799a75ef2ff.png)
![image](https://user-images.githubusercontent.com/61973814/143666377-0dd2723f-3783-4521-934a-fd70a64e9e3b.png)


Guanhao

![image](https://user-images.githubusercontent.com/61973814/143666393-d6066ed5-ebf3-4e62-a15b-7f5791ff59e4.png)
![image](https://user-images.githubusercontent.com/61973814/143666403-5674da49-6811-4929-9196-797473016e82.png)


Oiimo

![image](https://user-images.githubusercontent.com/61973814/143666412-73a59c9a-5658-4176-9492-698ce9f7b87e.png)


Alabasta

![image](https://user-images.githubusercontent.com/61973814/143666425-6409c1ba-683e-4138-b3ef-7ce5b66a62f7.png)


Seastone

![image](https://user-images.githubusercontent.com/61973814/143666431-1e78c064-2e79-4e36-83a0-a3f3b1d1ebaa.png)

CIDR GNS 3

![image](https://user-images.githubusercontent.com/73151831/143680640-7b645ae6-bd50-40b2-8df6-e26d73547c2f.png)

Config IP

Foosha
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.44.192.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.44.64.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.44.196.1
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.47.160.1
	netmask 255.255.255.252
```

Blueno
```
auto eth0
iface eth0 inet static
	address 10.44.192.2
	netmask 255.255.252.0
  gateway 10.44.192.1
```

Water7
```
auto eth0
iface eth0 inet static
	address 10.44.64.2
	netmask 255.255.255.252
  gateway 10.44.64.1

auto eth1
iface eth1 inet static
	address 10.44.32.1
	netmask 255.255.252.0
  gateway 10.44.64.1

auto eth2
iface eth2 inet static
	address 10.44.16.1
	netmask 255.255.255.252
  gateway 10.44.64.1
```

Cipher
```
auto eth0
iface eth0 inet static
	address 10.44.32.2
	netmask 255.255.252.0
  gateway 10.44.32.1
```

Pucci
```
auto eth0
iface eth0 inet static
	address 10.44.16.2
	netmask 255.255.255.252
  gateway 10.44.16.1

auto eth1
iface eth1 inet static
	address 10.44.0.1
	netmask 255.255.248.0
  gateway 10.44.16.1

auto eth2
iface eth2 inet static
	address 10.44.8.1
	netmask 255.255.255.128
  gateway 10.44.16.1
```

Jipangu
```
auto eth0
iface eth0 inet static
	address 10.44.8.2
	netmask 255.255.255.128
  gateway 10.44.8.1
```

Courtyard
```
auto eth0
iface eth0 inet static
	address 10.44.0.2
	netmask 255.255.248.0
  gateway 10.44.0.1
```

Calmbelt
```
auto eth0
iface eth0 inet static
	address 10.44.0.3
	netmask 255.255.248.0
  gateway 10.44.0.1
```

Doriki
```
auto eth0
iface eth0 inet static
	address 10.44.196.2
	netmask 255.255.255.252
  gateway 10.44.196.1
```

Guanhao
```
auto eth0
iface eth0 inet static
	address 10.44.160.2
	netmask 255.255.255.252
	gateway 10.44.160.1

auto eth1
iface eth1 inet static
	address 10.44.148.1
	netmask 255.255.252.0
	gateway 10.44.160.1

auto eth2
iface eth2 inet static
	address 10.44.136.5
	netmask 255.255.255.252
	gateway 10.44.160.1

auto eth3
iface eth3 inet static
	address 10.44.144.1
	netmask 255.255.254.0
	gateway 10.44.160.1
```

Jabra
```
auto eth0
iface eth0 inet static
	address 10.44.148.2
	netmask 255.255.252.0
	gateway 10.44.148.1
```

Maingate
```
auto eth0
iface eth0 inet static
	address 10.44.144.2
	netmask 255.255.254.0
	gateway 10.44.144.1
```

Alabasta
```
auto eth0
iface eth0 inet static
	address 10.44.144.3
	netmask 255.255.254.0
	gateway 10.44.144.1

auto eth1
iface eth1 inet static
	address 10.44.146.1
	netmask 255.255.255.240
	gateway 10.44.144.1
```

Jorge
```
auto eth0
iface eth0 inet static
	address 10.44.146.2
	netmask 255.255.255.240
	gateway 10.44.146.1
```

Oiimo
```
auto eth0
iface eth0 inet static
	address 10.44.136.6
	netmask 255.255.255.252
	gateway 10.44.136.5

auto eth1
iface eth1 inet static
	address 10.44.136.1
	netmask 255.255.255.252
	gateway 10.44.136.5

auto eth2
iface eth2 inet static
	address 10.44.132.1
	netmask 255.255.255.0
	gateway 10.44.136.5
```

Fukurou
```
auto eth0
iface eth0 inet static
	address 10.44.136.2
	netmask 255.255.255.252
	gateway 10.44.136.1
```

Enieslobby
```
auto eth0
iface eth0 inet static
	address 10.44.132.2
	netmask 255.255.255.0
	gateway 10.44.132.1
```

Seastone
```
auto eth0
iface eth0 inet static
	address 10.44.132.3
	netmask 255.255.255.0
	gateway 10.44.132.1

auto eth1
iface eth1 inet static
	address 10.44.128.1
	netmask 255.255.252.0
	gateway 10.44.132.1
```

Elena
```
auto eth0
iface eth0 inet static
	address 10.44.128.2
	netmask 255.255.252.0
	gateway 10.44.128.1
```
