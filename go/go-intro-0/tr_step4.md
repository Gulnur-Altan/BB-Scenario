
## Kodları Yazarken

### Yüklemeler
1- İlk Yapılması gereken shell ortamına ilgili paketleri yüklemektir.
Not: Bu adımı her senaryo açtığınızda yapmalısınız. Oturum kapatıldığında ortam sıfırlanmaktadır.

Her yeni senaryoda ilgili yüklemeleri yaparak, komutlara aşinalık kazanmanız hedeflenmektedir.

*apk add go*    İlgili Go Paketini imaja yükler.

*apk add nano*  Nano text editörünü yükler,oldukça kullanışlıdır.
(İpucu: *Ctrl* + *X* çık,ardından *Y* ile değişiklikleri kaydet ve çık)

Bunun yanında,

*vi*  
*vim*
editörleri de tecih edilebilir.
(İpucu: *i* ile Insert Mode aktif edilir,kodla *Esc* ile çık + *:wq* yaz + ardından *enter* kaydet ve çık)


## Terminal

Sağ tarafta bulunan Teminal ekranında Alphine Linux imajını kullanacaksınız.
Kodları yazdıktan sonra execute etmeniz beklenmektedir.Bunun için,
*go run xxx.go*
xxx ile belirtilen kısma dosya ismi yazılmalıdır.
Ya da,
*go chmod u+x xxx.go*
dosyaya izin vererek
*./xxx.go*
şeklinde de execute edebilirsiniz.


## Editör

Editör sayfasında Go dilini seçerek kodlama yapabilirsiniz
![editör2.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/editor2.PNG)

Kopyalama iconuna tıklayarak yazdığınız kodu kopyalayabilir,kaydedebilirsiniz.

![copy_icon.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/copy_icon.PNG)

Yandaki taşı iconu ile yazdığınız kodu shell e atabilirsiniz.

![share_icon.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/share_icon.PNG)

Unutmayın yazılan kodu oluşturduğunuz *xxx.go* sayfasının içine atmalısınız,node a değil ⚠️

# Node 

+ İconuna tıklayarak yeni terminal açabilirsiniz.
![node.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/node.PNG)

Açtığınız terminalde yüklemeleri aynı şekilde yapmalısınız.
Paketleri sonradan yüklediğiniz için ,yükleme olmadan komutlar çalışmayabilir.
İlgili porta ilerlemek için port ikonuna tıklamalısınız.

![port_icon.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/go_port_icon.PNG)
