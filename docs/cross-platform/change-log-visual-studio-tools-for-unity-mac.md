---
title: Değişiklik günlüğü (Unity, Mac için Visual Studio Araçları) | Microsoft Docs
ms.custom: ''
ms.date: 09/18/2019
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 33a6ac54-d997-4308-b5a0-af7387460849
author: therealjohn
ms.author: johmil
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 897851055bd2eacc10edea9fdff2ab3ecd61b963
ms.sourcegitcommit: 88f576ac32af31613c1a10c1548275e1ce029f4f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "71185970"
---
# <a name="change-log-visual-studio-tools-for-unity-mac"></a>Değişiklik Günlüğü (Unity için Visual Studio Araçları, Mac)

Değişiklik günlüğü Unity için Visual Studio Araçları.

## <a name="2330"></a>2.3.3.0

Yayın tarihi, 23 Eylül 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - IDE 'nin kullanılmayan parametreleri kaldırmak üzere hızlı bir çözüm göstermesini engellemek için, IDE0060 için yeni bir supprescursor eklendi.
    - `USP0005`için `IDE0060`: Unity iletileri Unity çalışma zamanı tarafından çağrılır.

## <a name="2320"></a>2.3.2.0

Yayın tarihi, 16 Eylül 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Unity 'ye özgü yeni Tanılamalar ekleyerek, Visual Studio 'nun Unity projelerine yönelik olduğunu anlama konusunu sunuyoruz. Unity projeleri için geçerli olmayan genel C# tanılamalarını gizleyerek IDE’yi daha akıllı hale getirdik. Örneğin, IDE, Unity düzenleyicisinde değişkeni değiştirmenize engel olacak bir Inspector değişkenini `readonly` değiştirmek için hızlı bir çözüm göstermez.
    - `UNT0001`: Unity iletileri, boş olsalar bile çalışma zamanı tarafından çağrılır. Unity çalışma zamanının bunları işlemek için gereksiz yere zaman harcamaması için bunları bildirmeyin.
    - `UNT0002`: Dize eşitliği kullanarak etiket karşılaştırması yapma, yerleşik CompareTag yönteminden daha yavaştır.
    - `UNT0003`: Tür güvenliği için, GetComponent’ın genel biçiminin kullanılması tercih edilir.
    - `UNT0004`: Güncelleştirme iletisi kare hızına bağlıdır ve Time.fixedDeltaTime yerine Time.deltaTime’ı kullanmalıdır.
    - `UNT0005`: FixedUpdate iletisi kare hızından bağımsızdır ve Time.deltaTime yerine Time.fixedDeltaTime kullanmalıdır.
    - `UNT0006`: Bu Unity iletisi için yanlış bir yöntem imzası algılandı.
    - `UNT0007`: Unity nesnelerine yönelik null karşılaştırma işleci, null birleşim ile uyumsuzdur ve Unity bunu geçersiz kılar.
    - `UNT0008`: Unity nesnelerine yönelik null karşılaştırma işleci, null yayma ile uyumsuzdur ve Unity bunu geçersiz kılar.
    - `UNT0009`: Bir sınıfa InitializeOnLoad özniteliği uygularken statik bir oluşturucu sağlamanız gerekir. InitializeOnLoad özniteliği, düzenleyici başlatıldığında bunun çağrılmasını sağlar.
    - `UNT0010`: MonoBehaviours yalnızca AddComponent() kullanılarak oluşturulmalıdır. MonoBehaviour bir bileşendir ve bunun GameObject’e eklenmesi gerekir.
    - `UNT0011`: ScriptableObject yalnızca CreateInstance() kullanılarak oluşturulmalıdır. Unity ileti yöntemlerinin işlenmesi için ScriptableObject’in Unity altyapısı tarafından oluşturulması gerekir.
    - `USP0001`için `IDE0029`: Unity nesneleri null birleşim kullanmamalıdır.
    - `USP0002`için `IDE0031`: Unity nesneleri null yayma kullanmamalıdır.
    - `USP0003`için `IDE0051`: Unity iletileri Unity çalışma zamanı tarafından çağrılır.
    - `USP0004`için `IDE0044`: SerializeField özniteliğine sahip alanlar ReadOnly yapılmamalıdır.

## <a name="2310"></a>2.3.1.0

Yayımlanma tarihi 4 Eylül 2019

### <a name="new-features"></a>Yeni Özellikler

- **Değerlendirme:**

  - Daha iyi tür görüntüleme desteği eklendi, yani `List<object>` `List'1[[System.Object, <corlib...>]]`yerine.

  - İşaretçi üye erişimi için destek eklendi, ör `p->data->member`.

  - Dizi başlatıcılarda örtük dönüştürmeler için destek eklendi, örn `new byte [] {1,2,3,4}`.

  - Bayt dizileri ve dizeleri incelenirken Onaltılı düzenleyici desteği eklendi.

## <a name="2300"></a>2.3.0.0

Yayın tarihi 13 Ağustos 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - Özel durumlarla düzeltilen Adımlama sorunları.

  - Sözde tanımlayıcıların ($exception gibi) sabit değerlendirmesi.

  - Geçersiz adreslerin başvurusu kaldırılırken kilitlenmeyi önleyin.  

  - Kaldırılmış AppDomain 'ler ile ilgili sorun düzeltildi.

## <a name="2200"></a>2.2.0.0

Yayın tarihi, 25 Temmuz 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - IntPtr türleriyle düzeltilen İnceleme.

- **Hata Ayıklayıcı:**

  - Catch noktaları ve işlev kesme noktalarının sabit işlenmesi.

## <a name="2130"></a>2.1.3.0

Yayın tarihi, 9 Temmuz 2019

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - Özel durumların yakalamak için destek eklendi.

  - MDS Protokolü 2,51 için destek eklendi.

- **Tümleştirme:**

  - Asmdef dosyaları için destek eklendi.

  - Şablondan bir dosya eklendiğinde yeniden adlandırma moduna geçin (Unity Düzenleyicisi davranışını taklit etmek için).

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Unity oynatıcılarla iletişim kurulurken hatalı biçimlendirilmiş iletilerin işlenmesi düzeltildi.

- **Değerlendirme:**

  - İfadelerde ad alanlarını sabit olarak işleme.

## <a name="2120"></a>2.1.2.0

Yayın 2 Temmuz 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - Ayrıştırılamayan ifadelerle düzeltilen hata raporlaması.

## <a name="2110"></a>2.1.1.0

Yayın tarihi, 27 Haziran 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Monodavranış API 'SI 2019,1 olarak güncelleştirildi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Sabit Unity Proje Gezgini performansı.

  - Hafif derleme etkinleştirildiğinde, çıktının düzeltilme uyarıları ve hataları düzeltildi.

  - Sabit basit derleme performansı.

## <a name="2100"></a>2.1.0.0

Yayın tarihi 20 Haziran 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - IntelliSense hatalarının ve uyarılarının kullanımı açısından Unity projelerinin tam derlemesini devre dışı bıraktı. Aslında Unity, dahili olarak hangi Unity 'nin yaptığını temsil eden sınıf kitaplığı projeleri içeren bir Visual Studio çözümü oluşturur. Bu şekilde, Visual Studio 'daki derlemenin sonucu, derleme işlem hattı kapalıyken Unity tarafından hiçbir şekilde kullanılmaz veya alınmaz. Visual Studio 'da oluşturma işlemi yalnızca hiçbir şey için kaynakları tüketiyor. Kendisine bağlı araçlara veya kuruluma sahip olduğunuz için tam bir yapıya ihtiyacınız varsa, bu iyileştirmeyi devre dışı bırakabilirsiniz (Unity için ayarlar/araçlar/projelerin tam derlemesini devre dışı bırak).
  
  - UPE içinde Unity paketleri için destek eklendi. Yalnızca başvurulan paketler ( `Packages` klasöründe manifest. JSON kullanılarak) ve yerel paketler ( `Packages` klasöre katıştırılmış) görünür.

## <a name="2021"></a>2.0.2.1

Yayımlanma tarihi 30 Mayıs 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Unity yürütme hedefleri için özel simge eklendi.

## <a name="2020"></a>2.0.2.0

Yayın 2 Nisan 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Kayıt sırasında Unity 'nin varlık veritabanının otomatik olarak yenilenmesi için destek eklendi. Bu, varsayılan olarak etkindir ve Visual Studio 'da bir betiği kaydederken Unity tarafında yeniden derleme tetikleyecektir. Kayıt sırasında Unity 'nin Assetveritabanını yenilemek için Tools\Options\Tools içinde bu özelliği devre dışı bırakabilirsiniz.

  - Çevrimdışı belgeler için tercih edilen Unity yüklemesinin ayarlanmasına yönelik destek eklendi.

  - Yeni düzenleyici için bağlam menüsü eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Boş çerçevelerle sabit derleme filtrelemesi ve çerçeve incelemesi.

## <a name="2011"></a>2.0.1.1
 
 Yayın tarihi 26 Mart 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Yalnızca bu çok özel yayın için mono varsayılan ve yalnızca kullanılabilir hata ayıklayıcı 'yı geçici olarak yapın.

## <a name="2006"></a>2.0.0.6

Yayın tarihi 26 Mart 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - "Unity 'ye Ekle ve Yürüt" desteği eklendi.

## <a name="2005"></a>2.0.0.5

Yayımlanma tarihi, 20 Mart 2019

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Çözüm dosyasını işlerken dış özellikleri koruyun.
  
- **Değerlendirme:**

  - Diğer ad nitelenmiş adlar için destek eklendi (şimdilik yalnızca genel ad alanı). Bu nedenle, ifade değerlendirici artık genel:: Namespace. Type biçimini kullanarak türleri kabul ediyor.

  - İşaretçi başvuru `pointer[index]` `*(pointer+index)` formuyla anlam ile aynı olan form için destek eklendi.

## <a name="2004"></a>2.0.0.4

Yayımlanma tarihi, 5 Mart 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - `ScriptableObject` API güncelleştirildi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Ad alanları şablonlardan kaldırıldı.

## <a name="2003"></a>2.0.0.3
 
 Yayımlanma tarihi, 5 Mart 2019

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Ortak ve serileştirilmiş alanlar artık uyarılara neden olmaz. Bu iletileri oluşturan Unity projelerinde `CS0649` ve `IDE0051` derleyici uyarılarını otomatik olarak gizliyoruz.

- **Tümleştirme:**

  - Bir Unity işlemi çalışıyorsa, belirli bir örneğe İliştirilmek için uyar.

- **Değerlendirme:**

  - Yerel işlevler için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Eski protokol sürümleri kullanılırken adlandırılmış bağımsız değişkenlerde özel öznitelik okuma düzeltildi.

## <a name="2002"></a>2.0.0.2

Yayımlanma tarihi 4 Şubat 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Monodavranış API 'SI güncelleştirildi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Hata ayıklayıcıda temel değerler ayarı düzeltildi.

## <a name="2001"></a>2.0.0.1

Yayın tarihi 4 Aralık 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Sabit yükleme paketi kendi kendine kapsama.

## <a name="2000"></a>2.0.0.0
 Yayın tarihi 4 Aralık 2018

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - Mac üzerindeki Unity hata ayıklayıcı, Windows 'daki aynı Core Unity hata ayıklayıcısıyla değiştirildi.

  - İfade değerlendirmesi için NRefactory 'ın Roslyn tarafından değiştirildiği yer.

  - İşaretçiler için destek eklendi: başvuru, atama ve işaretçi aritmetiği (Bu, hem Unity 2018.2 + hem de yeni çalışma zamanı için gereklidir).

  - Dizi işaretçisi görünümü (içinde C++olduğu gibi) için destek eklendi. Bir işaretçi ifadesi alın, sonra da bir virgül ve görmek istediğiniz öğe sayısını ekleyin.

  - Zaman uyumsuz yapılar için destek eklendi.

  - Sözde değişkenler (özel durum ve nesne tanımlayıcıları) için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Hatalı biçimlendirilmiş veya desteklenmeyen ifadelerle ifade değerlendirmesi düzeltildi.

## <a name="1700"></a>1.7.0.0

13 Kasım 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - Daha fazla istemci bilgileri (IP, makine adı) işleme İliştir iletişim kutusunda eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Visual Studio veya Unity, özellikle 'Unity İşleme İliştir' ulaşmaktan olduğunda dondurma yapma veya oyunu yeniden Unity'nın hata ayıklayıcısı altyapısı ile iletişim kurmak için kullanılan Kitaplığı'nda bir kilitlenme düzeltildi.

- **Tümleştirme:**

  - Başka bir varsayılan düzenleyici seçildiğinde sabit Unity eklentisini etkinleştirme.

  - Sabit Unity dosya şablonu oluşturma.

## <a name="1602"></a>1.6.0.2

24 Temmuz 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Unity tarafından sabit bir Unity performans hatanın geçici çözümü geri alındı.

## <a name="1601"></a>1.6.0.1

Yayın Tarihi: 10 Temmuz 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Sabit gölgelendirici kod coloration destekler.

## <a name="1600"></a>1.6.0.0

26 Haziran 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Sihirbazlar:**

  - Sabit yazım yanlışı OnApplicationFocus iletisi.

- **Proje oluşturma:**

  - Unity performans hatanın geçici çözüm: projeleri oluştururken MonoIslands önbellek.

  - Taşınabilir pdb mdb için artık yeni Unity çalışma zamanı kullanırken dönüştürmez.

## <a name="1502"></a>1.5.0.2

18 Nisan 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Temel gölgelendirici kod tamamlama desteği eklendi.

  - Gölgelendirici dosyaları açıklamalarda geçiş için destek eklendi.

## <a name="1501"></a>1.5.0.1

28 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Unity proje Gezgininde ek şablonlar için destek eklendi.

## <a name="1500"></a>1.5.0.0

21 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Algılama ve USB üzerinden bağlı Android oynatıcılarda ekleme desteği eklendi.

## <a name="1403"></a>1.4.0.3

5 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Yeni Proje Oluşturma Aracı'nda Unity 2018.1 desteği eklendi.

- **Tümleştirme:**

  - Özel ayarlar için eklenen seçeneği bölmesi.

## <a name="1402"></a>1.4.0.2

Yayın Tarihi: 24 Ocak 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Mono sürüm algılama düzeltildi.

- **Tümleştirme:**

  - 2018.1 ile zamanlama sorunları düzeltildi ve eklentisini etkinleştirme.

  - Yeni bir oynatıcı tespit edilirken sabit bildirimleri.

## <a name="1401"></a>1.4.0.1

23 Ocak 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Sabit Genişlet/Daralt klasörlerde çift tıklayın

## <a name="1400"></a>1.4.0.0

Yayın Tarihi: 13 Aralık 2017

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - .NET Standard için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Mdb hata ayıklama sembol dönüştürme sabit otomatik pdb.

## <a name="1301"></a>1.3.0.1

Yayın Tarihi: 12 Aralık 2017

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Dizi boyutu değiştirilmeye çalışılırken Inspector'ı etkileyen EditorPrefs.GetBool sabit dolaylı çağrı.

- **Sihirbazlar:**

  - Roslyn bağlam yöntemi eklemeden önce yenileyin.

## <a name="1300"></a>1.3.0.0

Yayın Tarihi: 20 Kasım 2017

### <a name="new-features"></a>Yeni Özellikler

- **Sihirbazlar:**

  - "Uygulama Unity ileti" Sihirbazı eklendi.

  - Yeni API vs'de için tamamlama Mac 7.4 desteği eklendi.

## <a name="1200"></a>1.2.0.0

Yayın Tarihi: 23 Ekim 2017

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - Taşınabilir hata ayıklama sembol dosyaları için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Ek .dll uzantısı yanlış derleme dosya adına eklenmiş düzeltildi.

  - Varsayılan 'true' olduğunda AllowAttachedDebuggingOfEditor Unity bayrağı zorlamaz.

## <a name="1103"></a>1.1.0.3

Yayın Tarihi: 23 Ekim 2017

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - .NET 4.6 profili için destek eklendi.

## <a name="1102"></a>1.1.0.2

Yayın Tarihi: 8 Ağustos 2017

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - İşleme İliştir'iletişim kutusunda emin değil, başlangıç iliştirmek için hangi Unity.

- **Proje oluşturma:**

  - Unity 5.6 kullanıldığında her zaman güvensiz derleme anahtar etkinleştirin.

## <a name="1101"></a>1.1.0.1

20 Temmuz 2017 tarihinde yayımlandı

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Yerelleştirilmiş kaynaklar için destek eklendi.

## <a name="1100"></a>1.1.0.0

12 Temmuz 2017 tarihinde yayımlandı

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Oyuncuların ve düzenleyicileri aracılığıyla ekleme işlemini penceresine ekleme desteği eklendi.

- **Proje oluşturma:**

  - Derleme adı başvuruları mcs.rsp dosyalarıyla düzeltildi.

  - Assembly.json derleme birimler için destek eklendi.

  - Sabit ile API düzeyleri tanımlar.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Derleme sırasında sabit gölgelendirici hata iletisi.

## <a name="1001"></a>1.0.0.1

4 Mayıs 2017 tarihinde yayımlandı

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Etkin belge izleme karma ve normal projeleri ile düzeltildi.

## <a name="1000"></a>1.0.0.0

3 Mayıs 2017 tarihinde yayımlandı
