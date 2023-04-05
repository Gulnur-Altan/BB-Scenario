### CTF 2.Senaryo

1. Github altında paylaşılan projeyi ilgili adresten ``/home/senaryolar/`` klasörü altına çekin. Klasör yoksa sizin oluşturmanız gerekmektedir.
```
https://github.com/merve-naz/BB-Senaryo-Dockerfile-Go.git 
```
2. Projeyi ilgili klasör altına çektikten sonra bu klasör altındaki dosyaları listeleyin. Proje dosyalarının orada olduğundan emin olun.

> Sizin için oluşturulan ortamda yüklü gelen "**git**" komutları ile bu işlemi  yapabilirsiniz. 

3. Burada "**BB-Senaryo-Dockerfile-Go**" adında bir klasör olacaktır. Bu github'dan cektigimiz projenin adıdır. Şimdi bu klasöründe içine gidiniz.

> İlgili dizinde bu dosyaların varlığından emin olun. Dosyalar yoksa bir yerde yanlış giden birşeyler olmuş demektir. 

```
DockerFile go.mod main.go
docker-compose.yaml go.sum public

```

4. Dockerfile dosyasındaki talimatları ve yönergeleri kullanarak bir Docker imajı oluşturmamız gerekiyor fakat burada verilen Dockerfile dosyasında eksik kısımlar var. İlk olarak bunu düzeltmelisiniz.

> DockerFile dosyasındaki standartları takip etmeniz gerekiyor. Eksik hatalı kısımları düzenlemelisiniz. 

5. Dockerfile dosyasını düzelttikten sonra artık docker build alabiliriz.(Docker imajı olustururken tag   verebilirsiniz. Bu senaryo için "latest" tagini kullanınız ) 

> DockerFile kullanarak build başlatmalısınız. Build işleminde "latest" tag ataması yapmalısınız. 

6. Imaj haline getirdiğiniz container dosyasını çalıştırabilirsiniz.

> Build aldığınız ve Imaj oluşturduğunuz uygulamanızı ayağa kaldırmanız gerekmektedir. 

7. Uygulamamız başarılı bir şekilde ayağa kalktıktan sonra containerın çalışıp çalışmadığını ve hangi portlara bağlandığını gözden geçirin.


8. Image içerisindeki dosyaları değiştirmek için ilgili komutu kullanarak çalışan bir Docker konteynerinin içine girebilirsiniz.

09. Dosya ve klasörleri gözden geçiriniz daha sonra public klasörüne gidiniz.

10. Public klasörünün içinde yer alan index.html dosyasını metin editörü ile açarak değiştirelim. "Hoşgeldiniz BB" yazısını "HOŞGELDİNİZ " olarak düzeltiniz.

- container içinden çıkalım. 

11. Docker containerını durdurun ve yeni oluşan imaj ile containerı ayağa kaldırın.

12. DockerHub'a olusturduğumuz bu imajı atmak için ilk olarak dockerhub websitesinden profil oluşturun.

13. Terminal ekranına asağıdaki komutu girin. Komut çalıstığı zaman üye oldugunuz kullanıcı adı ve şifreyi soracaktır.
``` 
docker login
```
15. Docker imajınızı Docker Hub'a yüklemek için, öncelikle imajınıza Docker Hub kullanıcı adınızı etiketlemeniz gerekir.( Eğer 6.adımda image olustururken bunu yaptıysanız buna gerek yoktur )

16. Docker image'ını Docker Hub'a push edin.
