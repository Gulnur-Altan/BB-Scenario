
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

Bir dosya oluşturmayı deneyin `vi golang.txt` ,içine random karakterler yazın ve kaydedin.
(İpucu: *i* ile Insert Mode aktif edilir,kodla *Esc* ile çık + *:wq* yaz + ardından *enter* kaydet ve çık)


## Editör

Sağ tarafta bulunan Editör ekranında Alphine Linux imajını kullanacaksınız.
Kodları yazdıktan sonra execute etmeniz beklenmektedir.Bunun için,

*go run xxx.go* komutu kullanılır  <br />
'xxx' ile belirtilen kısma dosya ismi yazılmalıdır.

Ya da,
*go chmod u+x xxx.go*  <br />
dosyaya izin vererek  <br />
*./xxx.go*  <br />
şeklinde de execute edebilirsiniz.

! Not : Terminale bir yazı kopyalamak için Ctrl + C , <br />
yapıştırırken  Ctrl + V komutlarını kullanabilirsiniz.


## Editör

Editör sayfasında Go dilini seçerek kodlama yapabilirsiniz

![editor.png](https://raw.githubusercontent.com/Gulnur-Altan/BB-Scenario/master/go/Assets/editor.PNG)


Unutmayın yazılan kodu *xxx.go* gibi go uzantılı sayfaya yazmalısınız ⚠️

# Terminal

Ctrl + Shift + " tıklayarak yeni terminal açabilirsiniz.

![terminal.png](https://raw.githubusercontent.com/Gulnur-Altan/BB-Scenario/master/go/Assets/terminal.PNG)

İlgili porta ilerlemek için sol taraftaki port ikonuna tıklamalısınız.

![port_icon.png](https://gitlab.bulutbilisimciler.com/bb-public/scenarios/-/raw/master/go/Assets/go_port_icon.PNG)
