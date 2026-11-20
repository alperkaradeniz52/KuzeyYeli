# Kuzey Yeli Örnek Veri Tabanı

BTK Akademi **Sıfırdan SQL Öğreniyorum** eğitiminde kullanılan örnek veri tabanının kurulum betiği.

Kuzey Yeli, Microsoft'un Northwind örnek veri tabanının Türkçe uyarlamasıdır. Bir ticaret şirketinin müşteri, ürün ve satış kayıtlarını içerir. Tablo ve sütun adları Türkçedir.

## İndirme

1. Bu sayfadaki dosya listesinde **KuzeyYeli.sql** dosyasına tıklayın.
2. Sağ üstteki **Download raw file** (aşağı ok simgesi) düğmesine tıklayın.
3. Dosyayı `C:\BTK\KuzeyYeli` klasörüne taşıyın.

Dosyayı Not Defteri gibi bir düzenleyicide açıp kaydetmeyin. Dosya UTF-8 kodlamalıdır. Farklı bir kodlamayla kaydedilirse Türkçe harfler bozulur.

## Kurulum

1. SQL Server Management Studio 22 ile sunucuya bağlanın.
2. **File > Open > File** (Ctrl+O) ile `KuzeyYeli.sql` dosyasını açın.
3. Hiçbir metin seçili değilken **F5** tuşuna basın.
4. Object Explorer'da **Databases** klasörüne sağ tıklayıp **Refresh** seçin.

Komut satırından kurmak için:

```
sqlcmd -S localhost -E -C -f 65001 -i C:\BTK\KuzeyYeli\KuzeyYeli.sql
```

> Uyarı: Sunucuda KuzeyYeli adlı bir veri tabanı varsa betik onu silip yeniden oluşturur.

## İçerik

| Tablo | Satır |
|---|---|
| Musteriler | 91 |
| Urunler | 77 |
| Kategoriler | 8 |
| Tedarikciler | 29 |
| Personeller | 9 |
| Satislar | 830 |
| Satis Detaylari | 2155 |
| Nakliyeciler | 3 |
| Bolge | 4 |
| Bolgeler | 53 |
| PersonelBolgeler | 49 |
| MusteriDemographics | 0 |
| MusteriMusteriDemo | 0 |

## Bu sürümdeki değişiklikler

- Veri tabanının adı KuzeyYeli yapıldı.
- SQL Server 2012 ile kaldırılan `sp_dboption` satırları çıkarıldı.
- Dosya UTF-8 olarak kaydedildi.

## Kaynak ve lisans

- Northwind: Microsoft, [sql-server-samples](https://github.com/microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs), MIT Lisansı
- Türkçe uyarlama: Musa UYUMAZ, [MU-SQL](https://github.com/MU-OldProjects/MU-SQL), MIT Lisansı

Ayrıntılar için `LICENSE` dosyasına bakın.
