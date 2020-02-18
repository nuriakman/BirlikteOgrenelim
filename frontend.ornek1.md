# Frontend Birlikte Çalışma Örneği

## Görev: Günübirlik Tur Sitesi

Bu çalışma projesinde amaç, bir turizm firması için günübirlik tur sitesi yapmaktır. Firmanın yaptığı işin detayları şunlardır:
- Firma, 10+ farklı konuma tur düzenlemektedir
- Her konumun bir kapak fotoğrafı vardır
- Her konum için açıklama vardır
- Her konum için 10+ resimden oluşan bir fotogaleri vardır.


## Yapılacak İşler
- Proje Lideri belirlenecek
- Lider, GitHub'da bir proje açılacak
- Lider, Proje ekibindekileri "Contributor" olarak projeye ekleyecek
- Lider, yapılamsı gerekn her işi projede oluşturacağı `yapilacak.isler.md` dosyasına yazacak
- Eğer, yapılacak iş için kişi seçimi yapılmışsa yanına yazacak
- Yapılacak işler `[ ]` ve tamamlanmış işler  `[x]` biçiminde işaretlenecek
- Projenin amacı, projeye eklenen her bir özellik `README.md` dosyasına uygun şekilde sunulacak
- Proje kapsamında kullanılacak Kapak Fotoğraları derlenecek ve "assets/kapak" dizini altına eklenecek
- Fotogaleriler için 01, 02, 03 vb adlarda klasörler açılıp içine derlenen fotoğraflar eklenecek
- Site için [Modern Bussines](https://startbootstrap.com/templates/modern-business/) adlı şablon kullanılacak
- Şablon indirilip parçalanacak (include komutu)
- Şablon parçalama dışında PHP kodu KULLANILMAYACAK! Proje tamamen STATİK SAYFALARDAN oluşacak
- Tur için gidilecek yere ait bir YouTube videosu bulunup bu video tur detayları sayfasında gösterilecek
- Hazırlanacak Sayfalar:
  - Ana sayfa
  - İletişim
  - Hakkımızda
  - Turlarımız
  - S.S.S. (Sıkça Sorulan Sorular)
  - Her tur için Tur Programı bilgileri olacak
  - Her tur için fotogaleri olacak
  - Gerek duyulan diğer sayfaları


## Dikkat Edilecekler
- Herkes yapılacak iş bölümüne göre çalışacak
- Editör olarak ATOM kullanılacak
- Commit/pull/push işlemleri ATOM üzerinden yapılacak
- Bilgisayarınızda çalışmaya başlamadan önce `git pull` yapmayı unutmayın
- Commit yaparken atomik bazda comit yapılmasına dikkat edilecek (4 saatlik çalışma 1 commit ile atılmayacak)
- Her commit sonrası `git push` ve `git pull` yapılmasına dikkat edilecek
- Aynı anda, aynı dosya üzerinde çalışmamaya dikkat edilecek
- Ekip üyeleri ile iletişim Telegram grubu üzerinden yapılacak
- Gerektiğinde Discord üzerinden toplantı düzenlenip neler yapıldığı anlatılacak
- Sisteme eklenecek resim dosyalarının boyutu en çok 300Kb olacak
- HTML kod geliştirilirken gereken her yere açıklamalar/yorum eklenecek


# Süreç boyunca edinilecek kazanımlar
## CSS
**Küçük Resim Kullanımı** Detaylı bilgi: [css3 object fit](https://www.w3schools.com/css/css3_object-fit.asp)
```html
<style>
.card-img-top {
    width: 100%;
    height: 15vw;
    object-fit: cover;
}  
</style>
```

**Bootstrap CARD nesnesi için sabit yükseklik verme**
```HTMK
<div class="card h-100">
```

## Toplu dosya boyutu değiştirme
### Yöntem 1

Aktif klasördeki dosyaları `yeni` adlı klasöre yeniden boyutlandırma

```BASH
mkdir yeni
for i in *.jpg; do convert $i -resize 800x600 yeni/$i;done
```
### Yöntem 2
Aktif klasördeki dosyaları yeniden boyutlandırma

```BASH
mogrify -resize 800x *.jpg
find . -name '*.jpg' -execdir mogrify -resize 800x {} \;
```

### Yöntem 3
Aktif klasör ve altındaki TÜM dosyaları yeniden boyutlandırma

```BASH
find . -name '*.jpg' -execdir mogrify -resize 800x {} \;
```

Resim oranlarının korunması hakkında: https://www.imagemagick.org/Usage/resize/#resize





