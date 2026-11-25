# javac ve javap Örnekleri

Java dosyalarının IDE kullanmadan, komut satırından `javac` ile derlenip `java` ile çalıştırılmasını ve
`javap` ile derlenmiş sınıfın incelenmesini gösteren küçük örnekler.

> **Not:** Bu depo 2017 yılında eğitim amaçlı yazıldı ve artık güncellenmiyor.

## İçerik

| Klasör | Ne yapar |
|---|---|
| `single/` | Paketsiz tek bir sınıf (`Deneme1`); ekran görüntüsü: `single/singleTerminal.PNG` |
| `paket/` | `paket` paketindeki iki sınıf; `Deneme1`, `Deneme2`'nin metodunu çağırır. Ekran görüntüsü: `paketTerminal.PNG` |
| `javap/` | `javap` ile incelenecek basit sınıf; ekran görüntüsü: `javap/javapInfo.PNG` |

## Teknolojiler

- Java (JDK), harici bağımlılık yok

## Çalıştırma

### Tek bir sınıfı derleyip çalıştırma

```bash
cd single
javac Deneme1.java
java Deneme1
```

### Paket içindeki sınıfları derleyip çalıştırma

Komutlar deponun kök klasöründen çalıştırılır; sınıf, paket adıyla birlikte verilir.

```bash
javac paket/*.java
java paket.Deneme1
```

Windows komut isteminde yol ayracı olarak `paket\*.java` yazılabilir.

### Kaynak yolu, jar ve çıktı klasörü vermek

Genel kullanım şekli (yollar örnektir):

```bash
javac -sourcepath src -cp kutuphane.jar:. paketim/Sinif.java -d classes
```

Windows'ta sınıf yolu ayracı `:` yerine `;` olur.

### javap

`javap`, derlenmiş bir sınıfın içeriği hakkında bilgi verir; `-c` seçeneği bayt kodunu da gösterir.

```bash
cd javap
javac Deneme1.java
javap -c Deneme1
```
