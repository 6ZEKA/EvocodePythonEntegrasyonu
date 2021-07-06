# Evocode Python Entegrasyonu

Bu yazı Evocode ile birlikte Python kütüphanelerini kullanabilmeniz için gerekli adımları anlatacaktır.

## Gereksinimler

* Visual Studio Community Edition
* Python 3.5+

## Visual Studio Kurulumu

1. [https://visualstudio.microsoft.com/tr/vs/community/](https://visualstudio.microsoft.com/tr/vs/community/) adresinde "Visual Studio'yu İndirin" butonuna basın ve yükleyici dosyasını indirin.

2. İndirdiğiniz dosyayı çalıştırın ve "Continue" butonuna tıklayın.

   <img src="https://www.guru99.com/images/c-sharp-net/image003.png" alt="Download and Install Visual Studio" style="zoom:50%;" />

3. Yükleyici gerekli dosyaları indirene kadar bekleyin.

   <img src="https://www.guru99.com/images/c-sharp-net/image004.png" alt="Download and Install Visual Studio" style="zoom:50%;" />

4. Gelen pencerede "Visual Studio Community" versiyonunu için "Install" butonuna tıklayın.

   <img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706094542566.png" alt="image-20210706094542566" style="zoom:50%;" />

5. Açılan pencerede "Universal Windows Platform Development", ".NET destop development" ve "Desktop development with C++" seçeneklerini onaylayın ve "Install" butotuna tıklayın. Yükleme süresi, internet bağlantınızın hızına ve bilgisayarınızın performansına göre değişiklik göstermektedir.

   <img src="https://www.guru99.com/images/c-sharp-net/image006.png" alt="Download and Install Visual Studio" style="zoom:50%;" />

6. Kurulum bittikten sonra bilgisayarınızı yeniden başlatın ve bir sonraki adıma geçin.

## Python Kurulumu

1. [https://www.python.org/downloads/windows/](https://www.python.org/downloads/windows/) adresinden istediğiniz Python versiyonunu indirin. Versiyonun en az 3.5 ve üstü olması gerekmektedir. İsterseniz doğrudan en güncel Python versiyonunu (bu yazının hazırlandığı gün itibariyle 3.9.6):

   * 32-bit sistemler için: [https://www.python.org/ftp/python/3.9.6/python-3.9.6.exe](https://www.python.org/ftp/python/3.9.6/python-3.9.6.exe)
   * 64-bit sistemler için: [https://www.python.org/ftp/python/3.9.6/python-3.9.6-amd64.exe](https://www.python.org/ftp/python/3.9.6/python-3.9.6-amd64.exe)

   linklerinden indirebilirsiniz.

2. İndirdiğiniz dosyası çalıştırın ve gelen ekranda alttaki iki seçeneği işaretleyip "Install Now"'a tıklayın.

   <img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706100700923.png" alt="image-20210706100700923" style="zoom:50%;" />

   

3. Yüklemenin tamamlanmasını bekleyin.

## Örnek Kodun Derlenmesi

Örnek kodun derlenmesi için Python'da `finta` kütüphanesinin kurulu olması gerekmektedir. Kurulum için başlat menüsünden bir "Komut İstemi (Command Prompt)" açın ve aşağıdaki komutu çalıştırın (Python'un kurulu olduğu dizine göre komut değişebilir):

``````
"C:\Program Files\Python39\python.exe" -m pip install finta
``````

<img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706101337865.png" alt="image-20210706101337865" style="zoom:50%;" />

[https://github.com/6ZEKA/EvocodePythonEntegrasyonu/blob/main/Examples-master.zip](https://github.com/6ZEKA/EvocodePythonEntegrasyonu/blob/main/Examples-master.zip) adresinden örnek VS çözümünü indirin ve bir klasöre açın. Klasördeki `Examples.sln` dosyasına çift tıklayın ve çözümü Visual Studio'da açın.

<img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706102958367.png" alt="image-20210706102958367" style="zoom:50%;" />

Sağ taraftaki çözüm ekranında Examples'ı genişletin ve `UsePythonExample` projesini genişletin.

<img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706103415685.png" alt="image-20210706103415685" style="zoom: 50%;" />

Burada iki konfigürasyon gereklidir:

1. `pythonPath.txt` dosyasına Python'un kurulu olduğu konumu yazmalısınız, örneğin

   ```C:\Windows\py.exe```

2. `scriptPath.txt` dosyasına Python betiklerinin (script) konumlanacağı adres yazılmalıdır, örneğin

   ```C:\Users\murat\Documents\Makinali\My scripts\bin\Indicators\pyscripts```

Bu iki dosya daha sonra Makinalı'nın kurulu olduğu dizine (varsayılan olarak `C:\Users\murat\AppData\Roaming\Makinali`) klasörüne kopyalanmalıdır.

Bu adımlar tamamlandıktan sonra, Visual Studio'da `UsePythonExample` projesine sağ tıklayıp `Build` seçeneği seçilmelidir.

<img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706104238400.png" alt="image-20210706104238400" style="zoom:50%;" />

Hiç bir hata olmaması durumunda, ekranın alt kısmında yer alan Output bölümünde `1 Successed` mesajı yer alacaktır.

<img src="C:\Users\murat\AppData\Roaming\Typora\typora-user-images\image-20210706104337207.png" alt="image-20210706104337207" style="zoom:67%;" />

Derlenen indikatörü/stratejiyi Makinalı'ya kopyalamak için; `Examples\UsePythonExample\bin\Debug` altındaki dosyalar, `C:\Users\murat\Documents\Makinali\My scripts\bin\Indicators` klasörüne; `Examples\UsePythonExample\bin\Debug\pyscripts` altındaki dosyalar ise, `scriptPath.txt` dosyasında belirttiğiniz klasör altına kopyalanmalıdır.



Tüm adımlar başarılı olarak tamamlandığı zaman, indikatör/strateji Makinalı programında gözükecektir.