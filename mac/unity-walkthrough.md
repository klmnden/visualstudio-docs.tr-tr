---
title: Unity ile oyunlar oluşturmaya başlamak, Mac için Visual Studio'da alma
description: Mac için Visual Studio ve Unity ile çalışmaya başlama
author: asb3993
ms.author: amburns
ms.date: 05/20/2019
ms.topic: article
ms.technology: vs-ide-general
ms.assetid: D07FA43B-9D18-4DFA-8343-CD538FAD84DB
ms.openlocfilehash: 8f14d21468336dba220a76ad8978f136d50f96f1
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66836397"
---
# <a name="getting-started-building-games-with-unity-in-visual-studio-for-mac"></a>Unity ile oyunlar oluşturmaya başlamak, Mac için Visual Studio'da alma 

Unity oyunlar geliştirmek sağlayan bir oyun altyapısı olan C#. Bu izlenecek yol, Visual Studio Mac ve Visual Studio için Mac için araçları için Unity uzantıyla Unity ortamına birlikte kullanarak hata ayıklama Unity oyunları ve geliştirmeye başlamak nasıl gösterir.

Visual Studio Unity için Mac araçları için Mac için Visual Studio ile yüklü bir ücretsiz bir uzantıdır Ancak, hata ayıklama özellikleri ve daha iyi IntelliSense desteği dahil olmak üzere Mac için Visual Studio üretkenlik özelliklerinden yararlanmak Unity geliştiricileri etkinleştirir.

## <a name="objectives"></a>Amaçlar

> [!div class="checklist"]
> * Mac için Visual Studio ile Unity geliştirme hakkında bilgi edinin

## <a name="prerequisites"></a>Önkoşullar

- Mac için Visual Studio ([https://www.visualstudio.com/vs/mac](https://www.visualstudio.com/vs/visual-studio-mac))
- Unity 5.6.1 Kişisel sürümü veya üzeri ([https://store.unity.com](https://store.unity.com/), çalıştırılacak unity.com hesabı gerektirir)

## <a name="intended-audience"></a>Hedef kitle

Bu Laboratuvar, alışkın olan geliştiricilerin yönelik C#, ancak deneyime gerekli değildir.

## <a name="task-1-creating-a-basic-unity-project"></a>Görev 1: Temel bir Unity projesi oluşturma

1. Başlatma **Unity**. İstenirse oturum açın.

2. **Yeni**'yi tıklatın.

    ![Unity yeni düğmesi](media/unity-image1.png)

3. Ayarlama **proje adı** için **"UnityLab"** seçip **3B**. Tıklayın **proje oluştur**.

    ![Yeni Proje ekran oluşturma](media/unity-image2.png)

4. Artık varsayılan Unity arabirimin bakıyorsunuz. Solda, ortada, proje dosyaları bölmesinde denetçisi ve alt ve sağ Hizmetleri gösterilen boş Sahne 3B görünümü ile oyun nesneleri Sahne hiyerarşisi vardır. Elbette, daha için çok daha fazla, ancak birkaç önemli bileşenlerin olanlardır.

    ![boş unity arabirimi](media/unity-image3.png)

5. Unity için yeni geliştiriciler için uygulamanızı çalıştıran her şeyi bağlamında mevcut bir **Sahne**. Sahne dosyasını türlerdeki projede geçerli görünüme ve özellikleri için kullanılan kaynaklar hakkında meta veriler içeren bir tek dosyadır. Bir platform için uygulama paketini, sonuçta elde edilen uygulama bir veya daha fazla sahneler yanı sıra, eklediğiniz herhangi bir platforma bağımlı kod koleksiyonu olan yukarı sona erecek. Bir projedeki istenen sayıda Sahne olabilir.

6. Yeni bir Sahne yalnızca bir kamera ve bir Yönlü ışık vardır. Sahne gerektiren bir **kamera** görünür olmasını her şey için ve bir **ses dinleyici** sesli olarak her şey için. Bu bileşenler eklenmiş bir **GameObject**.

7. Seçin **ana kamera** nesnesinden **hiyerarşi** bölmesi.

    ![Hiyerarşi bölmesinden test paketini vurgulanmış ana kamera nesnesi](media/unity-image4.png)

8. Seçin **denetçisi** özelliklerini gözden geçirmek için pencerenin sağ tarafındaki bölmeden. Dönüştürme bilgileri, arka plan, projeksiyon türü, görünüm alanı ve benzeri Kamera özellikleri içerir. Bir ses dinleyici bileşen de aslında kameraya bağlı sanal bir mikrofon Sahne seslerden işler varsayılan olarak eklendi.

    ![Inspector bölmesi](media/unity-image5.png)

9. Seçin **Yönlü ışık** nesne. Bu açık sahneye sağlar, böylece gölgelendiricileri gibi bileşenleri nesnelerini işleyin biliyorsunuz.

    ![Vurgulanan yönü ışık nesnesi](media/unity-image6.png)

10. Kullanım **denetçisi** görmeyi tür, renk, yoğunluğu, gölge türü vb. dahil olmak üzere genel Aydınlatma özellikleri içerir.

    ![Özellikler bölmesinde denetçisi bakarak](media/unity-image7.png)

11. Unity projeleri, Visual Studio Mac ortaklarınıza için biraz farklı tablonuzu önemlidir. İçinde **proje** sekme ve en altında sağ tıklatın **varlıklar** klasörü ve select **Finder'da Göster**.

    ![Bulucu bağlamı eylemi Göster](media/unity-image8.png)

12. Projeleri içeren **varlıklar**, **Kitaplığı**, **ProjectSettings**, ve **Temp** aynı klasör görebilirsiniz. Ancak, arabiriminde görünür olan tek hesaptır **varlıklar** klasör. **Kitaplığı** klasör yerel önbelleğe alınan varlıkları; varlıkları için tüm meta veriler tutar. **ProjectSettings** klasör, yapılandırabileceğiniz ayarlar depolar. **Temp** klasör kullanılan Mono ve Unity geçici dosyaları için derleme işlemi sırasında. Mac için Visual Studio'da açarak bir çözüm dosyası de mevcuttur (**UnityLab.sln** burada).

    ![Bulucu varlıkları](media/unity-image9.png)

13. Kapat **Bulucu** penceresi ve geri dön **Unity**.

14. **Varlıklar** klasörü tüm, varlıkları ve son teknoloji ürünü, kod, ses, vb. içerir. Artık boşsa, ancak her tek dosyayı projenize Getir buraya gelecek. Bu her zaman en üst düzey dizindir **Unity Editor**. Ancak, her zaman ekleme ve Unity arabirimi (veya Mac için Visual Studio) aracılığıyla dosyaları kaldırma ve hiçbir zaman doğrudan dosya sistemi üzerinden.

    ![unity klasöründe varlıklar](media/unity-image10.png)

15. **GameObject** gibi neredeyse her şeyi modelleri, ışık, parçacık sistemleri vb. dahil olmak üzere bu türünden türetilen Unity geliştirme için önemlidir. Yeni bir **küp** nesneyi sahneye **GameObject > 3B nesneye > Küp** menüsü.

    ![Küp nesne sahnede](media/unity-image11.png)

16. Yeni özelliklerini hızlı bir göz atın **GameObject** ve adı, etiket, katman ve dönüştürme olduğunu görürsünüz. Bu özelliklerin tümü için ortak olan **GameObjects**. Ayrıca, birçok bileşen eklendiği **küp** işlevleri dahil olmak üzere mesh filtre kutusu collider ve işleyici sağlamak için.

    ![Oyun nesne özellikleri](media/unity-image12.png)

17. Yeniden adlandırma **küp** adına sahip nesne, **"Küp"** varsayılan olarak, için **"İkincisinde"** . Basın emin **Enter** yapılan değişiklik kaydedilemiyor. Bu, bizim basit oyun rakip küpte olacaktır.

    ![Küp nesnesi yeniden adlandırma özelliği](media/unity-image13.png)

18. Başka bir **küp** nesnesi aynı işlemi olarak yukarıdaki kullanarak sahneye ve bu ad **"Player"** .

    ![İkinci küp nesneyi yeniden adlandırma](media/unity-image14.png)

19. Etiket için player nesnesine **"Player"** de (bkz **etiketi** aşağı açılır denetimin tam ad alanı altında). Bu rakip betikte player oyun nesneyi bulmak amacıyla kullanacağız.

    ![için player nesnesine etiketleme](media/unity-image15.png)

20. İçinde **Sahne** görüntülemek için rakip nesneyi fareyi kullanarak Z ekseni boyunca ayrılmak için player nesnesine taşıyın. Seçip sürükleyerek küp tarafından Z ekseni boyunca hareket kendi **kırmızı** doğru panelinde **mavi** satır. Küp 3B alanda yaşar, ancak yalnızca 2B'de her zaman sürüklenebilir beri sürükleyin, eksen özellikle önemlidir.

    ![Sahne görünümü gösteren küpü](media/unity-image16.png)

21. Aşağı ve sağa doğru ekseni küpe taşıyın. Bu güncelleştirmeleri **Transform.Position** özelliğinde **denetçisi**. Sonraki adımlar laboratuvarda kolaylaştırmak için burada gösterilen benzer şekilde bir konuma sürükleyin emin olun.

    ![bir küp ekseni boyunca hareket](media/unity-image17.png)

22. Şimdi, böylece player pursues rakip mantıksal sürücü için kod ekleyebilirsiniz. Sağ **varlıklar** klasöründe **proje** paneli ve seçin **Oluştur > C# betik**.

    ![C#betik bağlamı eylemi](media/unity-image18.png)

23. Yeni ad C# betik **"EnemyAI"** .

    ![C# betiği](media/unity-image19.png)

24. Oyun nesnelerine betikler eklemek için yeni oluşturulan kodun üzerine sürükleyin **ikincisinde** nesnesine **hiyerarşi** bölmesi. Artık bu nesne bu betiğin davranışları kullanacak.

    ![Oyun nesnesine ekleniyor betik gösteren vurgulama](media/unity-image20.png)

25. Seçin **Dosya > Kaydet sahneler** geçerli görünüme kaydetmek için. Adlandırın **"MyScene"** .

## <a name="task-2-working-with-visual-studio-for-mac-tools-for-unity"></a>Görev 2: Unity için Mac araçlar için Visual Studio ile çalışma

1. Düzenlemek için en iyi yolu C# kodu Mac için Visual Studio'yu kullanma Mac için Visual Studio, varsayılan işleyici olarak kullanılacak Unity yapılandırabilirsiniz. Seçin **Unity > Tercihler**.

2. Seçin **dış Araçlar** sekmesi. Gelen **dış betik Düzenleyicisi** açılır menüsünde, select **Gözat** seçip **uygulamalar/Visual Studio.app**. Alternatif olarak, zaten varsa bir **Visual Studio** seçeneği, yalnızca seçin.

    ![Dış araçlar sekmede tercihleri](media/unity-image21.png)

3. Unity kullanacak şekilde yapılandırılmış artık **Mac için Visual Studio** betik düzenlemesi için. Kapat **Unity tercihleri** iletişim.

    ![VisualStudio tercihleri seçildi](media/unity-image22.png)

4. Çift **EnemyAI.cs** açılır **Mac için Visual Studio**.

    ![Unity içinde seçili rakip varlık](media/unity-image23.png)

5. Visual Studio çözümünü oldukça basittir. İçerdiği bir **varlıklar** klasörü (aynı bir **Bulucu**) ve **EnemyAI.cs** daha önce oluşturduğunuz betiği. Daha karmaşık projeler içinde hiyerarşi büyük olasılıkla içinde Unity görmek daha farklı görünecektir.

    ![Mac için Visual Studio'da Çözüm bölmesi](media/unity-image24.png)

6. **EnemyAI.cs** düzenleyicide açık. İlk komut, yalnızca için saplamalar içerir **Başlat** ve **güncelleştirme** yöntemleri.

7. İlk rakip kodu aşağıdaki kodla değiştirin.

    ```csharp
    public class EnemyAI : MonoBehaviour
    {
        public float Speed = 50;
        private Transform _playerTransform;
        private Transform _myTransform;
        
        void Start()
        {
            var player = GameObject.FindGameObjectWithTag("Player");
            if (!player)
            {
                Debug.LogError(
                    "Could not find the main player. Ensure it has the player tag set.");
            }
            else
            {
                _playerTransform = player.transform;
            }
            _myTransform = this.transform;
        }

        void Update()
        {
            var moveAmount = Speed * Time.deltaTime;
            _myTransform.position = Vector3.MoveTowards(_myTransform.position,
                _playerTransform.position, moveAmount);

            if (_myTransform.position == _playerTransform.position)
            {
                _myTransform.position = Vector3.back * 10;
            }
        }
    }
    ```

8. Hızlı tanımlanan basit rakip davranışını buraya göz atın. İçinde **Başlat** yöntemi aldığımız player nesnesine bir başvuru (etiketine göre), yanı sıra kendi **dönüştürme**. İçinde **güncelleştirme** her karede çağrılır, yöntem, ikincisinde için player nesnesine taşınır. Mac için Visual Studio'da kod tabanının anlamak daha kolay hale getirmek için renk kodlaması adları ve anahtar sözcükler kullanın

9. Rakip betik değişiklikleri kaydetmek **Mac için Visual Studio**.

## <a name="task-3-debugging-the-unity-project"></a>Görev 3: Unity proje hata ayıklama

1. Kod ilk satırında bir kesme noktası ayarlamak **Başlat** yöntemi. Düzenleyici kenar imlecin hedef satır veya yerde tuşuna basın ve satır tıkayın **F9**.

    ![mac için visual Studio'daki kesme noktası ayarlama](media/unity-image25.png)

2. Tıklayın **hata ayıklamayı Başlat** düğme veya basın **F5**. Bu projeyi oluşturun ve hata ayıklama için Unity'ye İliştir.

    ![mac için visual Studio'da Başlat düğmesi](media/unity-image26.png)

3. Geri dönüp **Unity** tıklatıp **çalıştırmak** oyun Başlat düğmesini.

    ![Unity Çalıştır düğmesi](media/unity-image27.png)

4. Kesme noktasına isabet ve Visual Studio artık Mac için hata ayıklama araçları kullanabilirsiniz.

    ![mac için visual Studio'da isabet kesme noktası](media/unity-image28.png)

5. Gelen **Yereller** paneli, bulun **bu** başvuran bir işaretçi bir **EnemyAI** nesne. Başvuru genişletin ve ilişkili üyeleri gibi göz atabilirsiniz bkz **hızı**.

    ![Yerel öğeler paneli mac için visual Studio'da hata ayıklama](media/unity-image29.png)

6. Kesme noktasından kaldırmak **Başlat** yöntemi olduğu aynı şekilde eklenen göre kenar boşluğunu tıklayarak ya da satır seçip ENTER tuşuna **F9**.

    ![mac için visual Studio'da isabet kesme noktası](media/unity-image30.png)

7. Tuşuna **F10** ilk bulan bir kod satırı üzerinden atlamak için **Player** parametre olarak bir etiket kullanarak oyun nesnesi.

8. Fare imleci üzerine **player** ilişkili üyelerini görüntülemek için kod düzenleyicisi penceresi içinde değişken. Alt özellikleri görüntülemek için katmana bile genişletebilirsiniz.

    ![Pencere Düzenleyicisi mac için visual Studio'da hata ayıklama](media/unity-image31.png)

9. Basın **F5** veya basın **çalıştırma** yürütmeye devam etmek için düğmeyi. Yaklaşan player küp rakip küp tekrar tekrar görmek için Unity dönün. Görünür değilse, kamera ayarlamanız gerekebilir.

    ![Sahne içinde Unity yürütülüyor](media/unity-image32.png)

10. Dönmek **Mac için Visual Studio** ilk satırında bir kesme noktası ayarlayın **güncelleştirme** yöntemi. Hemen isabet.

    ![mac için visual Studio'da bir kesme noktası ayarlama](media/unity-image33.png)

11. Hızı çok daha hızlıdır ve uygulamayı yeniden başlatmadan değişikliğin etkisini test etmek istediğimiz varsayalım. Bulun **hızı** içinde değişken **Otolar** veya **Yereller** penceresi ve olarak değiştirin **"10"** basın **Enter** .

    ![Yerel öğeler penceresinde değişkenleri ayarlama](media/unity-image34.png)

12. Kesme noktası kaldırıp tuşuna **F5** yürütme devam etmek için.

13. Geri dönüp **Unity** çalışan uygulamayı görüntülemek için. Rakip küp artık özgün hızı beşinci bir taşınıyor.

    ![uygulamayı çalıştıran ile unity penceresi](media/unity-image35.png)

14. Unity uygulamasını tıklayarak durdurun **Play** düğmesini tekrar.

    ![unity uygulaması durduruluyor](media/unity-image36.png)

15. Geri dönüp **Mac için Visual Studio**. Tıklayarak hata ayıklama oturumunu durdurun **Durdur** düğmesi.

    ![Mac için Visual Studio hata ayıklama oturumunda durduruluyor](media/unity-image37.png)

## <a name="task-4-exploring-unity-features-in-visual-studio-for-mac"></a>Görev 4: Mac için Visual Studio'da Unity özelliklerini keşfetme

1. Mac için Visual Studio Kod Düzenleyicisi içinde Unity belgeleri hızlı erişim sağlar. İmleç üzerinde yere yerleştirinceye **Vector3** içinde Sembol **güncelleştirme** yöntemi ve ENTER tuşuna **⌘ Command + '** .

    ![Düzenleyici mac için visual Studio'daki yöntemi seçme](media/unity-image38.png)

2. Belgelerine yeni bir tarayıcı penceresi açılır **Vector3**. Koşullar karşılanırsa tarayıcı penceresini kapatın.

    ![belgeler için tarayıcı penceresi açılır](media/unity-image39.png)

3. Mac için Visual Studio Unity davranışı sınıfları hızla oluşturmak için bazı Yardımcıları de sağlar. Gelen **Çözüm Gezgini**, sağ **varlıklar** seçip **Ekle > Yeni MonoBehaviour**.

    ![Yeni monobehaviour bağlamı eylemi](media/unity-image40.png)

4. Yeni oluşturulan sınıf için saplamalar sağlar **Başlat** ve **güncelleştirme** yöntemleri. Kapanış ayracı sonra **güncelleştirme** yöntemi, yazmaya başlayın **"onmouseup"** . Visual Studio IntelliSense Hızlı bir şekilde uygulamak için planlıyorsanız metodunda sıfırlar, siz yazarken dikkat edin. Sağlanan otomatik tamamlama listesinden seçin. Bir metot taslağı parametreleri dahil onu doldurur.

    ![mac için visual Studio IntelliSense](media/unity-image41.png)

5. İçinde **OnMouseUp** yöntemi, tür **"temel".** Tüm taban yöntemi çağırmak kullanılabilir görmek için. Farklı aşırı yüklemeler her işlevin IntelliSense çıkma sağ üst köşesinde disk belleği seçeneğini kullanarak da keşfedebilirsiniz.

    ![mac için visual studio içinde aşırı keşfetme](media/unity-image42.png)

6. Mac için Visual Studio kolayca yeni gölgelendiricileri tanımlamanızı sağlar. Gelen **Çözüm Gezgini**, sağ **varlıklar** seçip **Ekle > Yeni gölgelendirici**.

    ![mac için visual Studio'da yeni bir gölgelendirici eylemi](media/unity-image43.png)

7. Tam renk ve yazı tipi işleme okumanız ve anlamanız daha kolay hale getirmek için gölgelendirici dosyası biçimini alır.

    ![Söz dizimi vurgulama](media/unity-image44.png)

8. Geri dönüp **Unity**. Mac için Visual Studio ile aynı proje sistemi çalışır olduğundan, her iki yerde yapılan değişiklikleri otomatik olarak diğer eşitlendiğini görürsünüz. Artık her zaman en uygun aracı görev için kullanacağınız kolaydır.

    ![Unity varlık paneli](media/unity-image45.png)

## <a name="summary"></a>Özet

Bu laboratuvarda, Mac için Visual Studio ve Unity ile oyun oluşturmaya başlamak nasıl öğrendiniz. Bkz: [ https://unity3d.com/learn ](https://unity3d.com/learn) Unity hakkında daha fazla bilgi edinmek için.
