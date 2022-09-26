# Pemograman-Client-Server-Prakterk--Latihan2
## Langkah - Langkah Membuat Latihan 2
### Langkah 1 :
#### Buat proyek web menggunakan link berikut [start.spring.io](https://start.spring.io/) kemudian pilih Spring web dan kemudian bahasa java dan sesuaikan versinya dengan device (disini saya menggunakan jdk 17 kemudian isi artifactnya(saya menggunakan latihan2-service) kemudian spring bootversinya pakai yang versi 2.6.11(yang saya pakai) dan untuk grubnya isi dengan com.taufiq kemudian download dan extrack dari zip menjadi file kemudian import ke dalam apache netbean
### Langkah 2 :
#### Kemudian cari proyek yang bernama LatihanServiceApplication dibawah package com.taufiq.latihan2.service kemudian pada proyek itu masukkan code berikut : 
```java
package com.taufiq.microservices.latihan2.service;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class Latihan2ServiceApplication {

	public static void main(String[] args) {
		SpringApplication.run(Latihan2ServiceApplication.class, args);
	}
        @GetMapping("/hello")
            public String hello(@RequestParam(value = "name", defaultValue = "Latihan 2") String name) {
            return String.format("Hello %s!", name);
        }

}

```
### Langkah 3 :
#### Kemudian cari proyek aplication.properties yang berada di *Other Source >> src/main/resources >> >> aplication.properties* kemudian masukkan code berikut :
```java
server.port=8011
```
### Langkah 4 :
#### Terakhir untuk output buka chrome/browser lalu ketik local host sesuai port yang dibuat 
#### Link : [latihan2](http://localhost:8011/hello)
![Screenshot 2022-09-26 212031](https://user-images.githubusercontent.com/113502696/192300844-900fb50f-7a3b-4154-8655-9b81c79352f9.jpg)
