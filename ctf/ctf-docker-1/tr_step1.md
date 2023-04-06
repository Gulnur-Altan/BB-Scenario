# Workshop Docker

## 1) Ön Hazırlık
Bu adımımızda sizden beklentimiz ``/home/ctf-docker-1`` adında bir klasör oluşturmanızdır. 

## 2) Örnek Proje Kopyalama
Bu adımda sizden beklentimiz daha öncesinde oluşturduğunuz ``/home/ctf-docker-1`` klasörünün altında aşağıda linki verilen projeyi kopyalamanızdır. Bunun için "GIT" komutunu kullanabilirsiniz. 
``https://github.com/merve-naz/BB-Senaryo-Dockerfile-Go.git``

## 3) Dosya Kontrolleri
İkinci adımda  "/home/ctf-docker-1" dizini altında projemizin kopyalandığını kontrol etmeniz önerilmektedir. Tüm işlemleri doğru yaptıysanız bu dizin altında ``BB-Senaryo-Dockerfile-Go`` isminde bir dizin oluşması gerekecektir. 

3.1 Burada " BB-Senaryo-Dockerfile-Go" adında bir klasör  olacaktır. Bu github'dan cektigimiz projenin adıdır. Şimdi bu klasöründe içine girelim.

İlgili dizinde bu dosyaların varlığından emin olun. Dosyalar yoksa bir yerde yanlış giden birşeyler olmuş demektir.
 
- Dockerfile                  go.mod       main.go 
- docker-compose.yaml         go.sum       public


3.2 Bu aşamada sizden bir DockerFile'ı gözden geçirmeniz beklenmektedir.
DockerFile dosyasındaki standartları takip etmeniz gerekiyor. Eksik, hatalı kısımları düzenlemelisiniz.

- `vi`: Dosya içerik düzenleme

3.3 Dockerfile dosyasını düzelttikten sonra artık docker build alabilirsiniz. Build işleminde "latest" ile tag ataması yapmalısınız. ("d****" ile belirtilen komutu siz yazmalısınız. )

- `d**** ***** -t <yeni_image_name>:latest .`

3.4 Build aldığınız ve imaj oluşturduğunuz uygulamanızı ayağa kaldırmanız gerekmektedir.
(İpucu: Github'dan çekilen go projesinde main.go'ya bakarsak host_port:8080 olduğunu kontrol ediniz.)

- `d***** *** -p <host_port>:<container_port> --name <container_name> :latest`

3.5 Uygulamamız başarılı bir şekilde ayaga kalktı. Uygulamamızı içeren container'ın çalışıp çalışmadığını ve hangi portlara bağlandığını gözden geçiriniz.
 `****** ps ` 

3.6 Image içerisindeki dosyaları değiştirmek için docker exec -it komutu kullanarak bir çalışan bir Docker konteynerinin içine girebilirsiniz. Aşagıdaki komutu çalıştırın.
```
docker exec -it   my-container /bin/sh 
```

3.7 Public klasörünün içinde yer alan index.html dosyasını, metin editörü ile açarak değiştirelim. "Hoşgeldiniz BB" yazısına "HOŞGELDİNİZ " olarak düzeltiniz.

- container içinden çıkalım. 

3.8 Docker containerını durdurun ve yeni imaj oluşturun ,oluşan imaj ile containerı ayağa kaldırın.

- İpucu: Yeni imaj oluşturmadan önce eski imajı silmeniz gerekmektedir.
- `docker rmi`: İmaj silme

3.9 DockerHub'a olusturduğumuz bu imajı atmak için ilk olarak dockerhub websitesinden profil oluşturun.

3.10 Terminal ekranına asağıdaki komutu girin. Komut çalıstığı zaman üye oldugunuz kullanıcı adı ve şifreyi soracaktır.
``` 
docker login
```

3.11 Docker imajınızı Docker Hub'a yüklemek için, öncelikle imajınıza Docker Hub kullanıcı adınızı etiketlemeniz gerekir.( Eğer image olustururken bunu yaptıysanız buna gerek yoktur )

`docker tag <image_id or image_name> <Docker_Hub_Kullanıcı_Adı>/<Image_Adı>:latest`

3.12 Docker image'ını Docker Hub'a push edin.

