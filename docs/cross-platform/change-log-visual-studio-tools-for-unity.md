---
title: Değişiklik günlüğü (Unity, Windows için Visual Studio Araçları) | Microsoft Docs
ms.custom: ''
ms.date: 09/18/2019
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: ea490b7e-fc0d-44b1-858a-a725ce20e396
author: therealjohn
ms.author: johmil
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 713535bb11b4bd9cab4ef1b31507b96fe1c9897a
ms.sourcegitcommit: 88f576ac32af31613c1a10c1548275e1ce029f4f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "71185997"
---
# <a name="change-log-visual-studio-tools-for-unity-windows"></a>Değişiklik günlüğü (Unity, Windows için Visual Studio Araçları)

Değişiklik günlüğü Unity için Visual Studio Araçları.

## <a name="4330"></a>4.3.3.0

Yayın tarihi, 23 Eylül 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Basit derlemeler için düzeltilen hata ve uyarı raporlaması.

## <a name="4320"></a>4.3.2.0

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

## <a name="4310"></a>4.3.1.0

Yayımlanma tarihi 4 Eylül 2019

### <a name="new-features"></a>Yeni Özellikler

- **Değerlendirme:**

  - Daha iyi tür görüntüleme desteği eklendi, yani `List<object>` `List'1[[System.Object, <corlib...>]]`yerine.

  - İşaretçi üye erişimi için destek eklendi, ör `p->data->member`.

  - Dizi başlatıcılarda örtük dönüştürmeler için destek eklendi, örn `new byte [] {1,2,3,4}`.

## <a name="4300"></a>4.3.0.0

Yayın tarihi 13 Ağustos 2019

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - MDS Protokolü 2,51 için destek eklendi.

- **Tümleştirme:**

  - Sıralama, arama ve yenileme özellikleriyle "Unity örneğine Ekle" penceresi geliştirildi. PID artık yerel oyuncular için de görüntülenir (sahip olan işlemi almak için sistemdeki dinleme yuvaları sorgulanarak).

  - Asmdef dosyaları için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Unity oynatıcılarla iletişim kurulurken hatalı biçimlendirilmiş iletilerin işlenmesi düzeltildi.

- **Değerlendirme:**

  - İfadelerde ad alanlarını sabit olarak işleme.

  - IntPtr türleriyle düzeltilen İnceleme.
  
  - Özel durumlarla düzeltilen Adımlama sorunları.

  - Sözde tanımlayıcıların ($exception gibi) sabit değerlendirmesi.

  - Geçersiz adreslerin başvurusu kaldırılırken kilitlenmeyi önleyin.  

  - Kaldırılmış AppDomain 'ler ile ilgili sorun düzeltildi.

## <a name="4201"></a>4.2.0.1

Yayın tarihi, 24 Temmuz 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Unity Proje Gezgini 'nden herhangi bir tür dosya oluşturmak için yeni bir seçenek eklendi.
  
  - Unity projeleri için hızlı derlemeler kullanırken tanılama önbelleğe almayı geliştirme.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Dosya Uzantısı iyi bilinen herhangi bir düzenleyici tarafından işlenmediğinde bir sorun düzeltildi.

  - Unity proje Gezgininde özel uzantılar için sabit destek.

  - Ana iletişim kutusunun dışında sabit kaydetme ayarları.

  - Eski Microsoft. VisualStudio. MPF bağımlılığı kaldırıldı.

## <a name="4110"></a>4.1.1.0

Yayımlanma tarihi 24 Mayıs 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Monodavranış API 'SI 2019,1 olarak güncelleştirildi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Hafif derleme etkinleştirildiğinde, çıktının düzeltilme uyarıları ve hataları düzeltildi.

  - Sabit basit derleme performansı.

## <a name="4100"></a>4.1.0.0

Yayımlanma tarihi 21 Mayıs 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Projeleri daha hızlı yeniden yüklemek için yeni Batch API 'SI için destek eklendi.

  - IntelliSense hatalarının ve uyarılarının kullanımı açısından Unity projelerinin tam derlemesini devre dışı bıraktı. Aslında Unity, dahili olarak hangi Unity 'nin yaptığını temsil eden sınıf kitaplığı projeleri içeren bir Visual Studio çözümü oluşturur. Bu şekilde, Visual Studio 'daki derlemenin sonucu, derleme işlem hattı kapalıyken Unity tarafından hiçbir şekilde kullanılmaz veya alınmaz. Visual Studio 'da oluşturma işlemi yalnızca hiçbir şey için kaynakları tüketiyor. Kendisine bağlı araçlara veya kuruluma sahip olduğunuz için tam bir yapıya ihtiyacınız varsa, bu iyileştirmeyi devre dışı bırakabilirsiniz (Unity için Araçlar/Seçenekler/araçlar/projelerin tam derlemesini devre dışı bırak).

  - Unity projesi yüklendiğinde Unity Proje Gezgini 'ni (UPE) otomatik olarak gösterin. UPE Çözüm Gezgini yanına yerleştirilir.

  - Unity 2019. x ile güncelleştirilmiş proje adı ayıklama mekanizması.

  - UPE içinde Unity paketleri için destek eklendi. Yalnızca başvurulan paketler ( `Packages` klasöründe manifest. JSON kullanılarak) ve yerel paketler ( `Packages` klasöre katıştırılmış) görünür.

- **Proje oluşturma:**

  - Çözüm dosyasını işlerken dış özellikleri koruyun.

- **Değerlendirme:**

  - Diğer ad nitelenmiş adlar için destek eklendi (şimdilik yalnızca genel ad alanı). Bu nedenle, ifade değerlendirici artık genel:: Namespace. Type biçimini kullanarak türleri kabul ediyor.

  - İşaretçi başvuru `pointer[index]` `*(pointer+index)` formuyla anlam ile aynı olan form için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Microsoft. VisualStudio. MPF ile ilgili sabitlenmiş bağımlılık sorunları.

  - Yüklü bir proje olmadan sabit UWP oynatıcı iliştirme.

  - Visual Studio henüz iliştirilmediğinde düzeltilen otomatik varlık veritabanı yenilemesi.

  - Etiketler ve onay kutuları ile ilgili sabit Tema sorunları.

- **Hata Ayıklayıcı:**

  - Statik oluşturucularla düzeltilen Adımlama.

## <a name="4005"></a>4.0.0.5

Yayın tarihi, 27 Şubat 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Kurulum paketiyle Visual Studio sürüm algılaması düzeltildi.

  - Kullanılmayan derlemeler kurulum paketinden kaldırıldı.

## <a name="4004"></a>4.0.0.4

Yayın tarihi, 13 Şubat 2019

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Yükleme sırasında Unity süreçlerini düzgün bir şekilde algılamak ve kurulum altyapısının dosya kilitlerini daha iyi işlemesini sağlamak için destek eklendi.

  - `ScriptableObject` API güncelleştirildi.

## <a name="4003"></a>4.0.0.3

Yayın tarihi 31 Ocak 2019

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Ortak ve serileştirilmiş alanlar artık uyarılara neden olmaz. Bu iletileri oluşturan Unity projelerinde `CS0649` ve `IDE0051` derleyici uyarılarını otomatik olarak gizliyoruz.

- **Tümleştirme:**

  - Unity Düzenleyicisi ve oynatıcı örneklerini görüntülemek için Kullanıcı deneyimi geliştirildi (Windows artık yeniden boyutlandırılabilir, tek biçimli kenar boşlukları kullanıyor ve bir yeniden boyutlandırma tutamacı görüntülüyor). Unity düzenleyicileri için Işlem kimliği bilgileri eklendi.

  - `MonoBehaviour` API güncelleştirildi.

- **Değerlendirme:**

  - Yerel işlevler için destek eklendi.

  - Sözde değişkenler (özel durum ve nesne tanımlayıcıları) için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Bilinen ad görüntüleri ve temalarıyla ilgili bir sorun düzeltildi.

  - Varlık veritabanının otomatik olarak yenilenmesi sırasında hata ayıklama sırasında yalnızca Çıkış Penceresi yazın.

  - Monodavranış Sihirbazı filtrelemesinde sabit UI gecikmeleri.

- **Hata Ayıklayıcı:**

  - Eski protokol sürümleri kullanılırken adlandırılmış bağımsız değişkenlerde özel öznitelik okuma düzeltildi.

## <a name="4002"></a>4.0.0.2

Yayın tarihi, 23 Ocak 2019

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Deneysel derleme üretimi düzeltildi.

  - UI-iş parçacığı basıncını en aza indirmek için sabit proje dosyası olay işleme.

  - Toplu metin değişiklikleri ile sabit tamamlama sağlayıcısı.

- **Hata Ayıklayıcı:**

  - Kullanıcı hata ayıklama iletilerinin ekli hata ayıklayıcısına gösterilmesi düzeltildi.

## <a name="4001"></a>4.0.0.1

Yayın tarihi 10 Aralık 2018

### <a name="new-features"></a>Yeni Özellikler

- **Değerlendirme:**

  - İfade değerlendirmesi için NRefactory 'ın Roslyn tarafından değiştirildiği yer.

  - İşaretçiler için destek eklendi: başvuru, atama ve işaretçi aritmetiği (Bu, hem Unity 2018.2 + hem de yeni çalışma zamanı için gereklidir).

  - Dizi işaretçisi görünümü (içinde C++olduğu gibi) için destek eklendi. Bir işaretçi ifadesi alın, sonra da bir virgül ve görmek istediğiniz öğe sayısını ekleyin.

  - Zaman uyumsuz yapılar için destek eklendi.

- **Tümleştirme:**

  - Kayıt sırasında Unity 'nin varlık veritabanının otomatik olarak yenilenmesi için destek eklendi. Bu, varsayılan olarak etkindir ve Visual Studio 'da bir betiği kaydederken Unity tarafında yeniden derleme tetikleyecektir. Kayıt sırasında Unity 'nin Assetveritabanını yenilemek için Tools\Options\Tools içinde bu özelliği devre dışı bırakabilirsiniz.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Tercih edilen harici düzenleyici olarak Visual Studio seçilmediğinde, sabitlenmiş köprü etkinleştirme.

  - Hatalı biçimlendirilmiş veya desteklenmeyen ifadelerle ifade değerlendirmesi düzeltildi.

## <a name="4000"></a>4.0.0.0

Yayın tarihi 4 Aralık 2018

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Visual Studio 2019 için destek eklendi (Visual Studio 2019 ' i dış betik düzenleyicisi olarak kullanabilmeniz için en az Unity 2018,3 gerekir).

  - HDPı ölçeklendirme, piksel kusursuz görüntüler ve tema için tam destek sayesinde Visual Studio görüntü hizmeti ve kataloğunu benimseyen.

### <a name="deprecated-features"></a>Kullanım dışı Özellikler

- **Tümleştirme:**

  - Unity için Visual Studio Araçları, yalnızca Unity 5.2 + ' ı destekler (Unity 'nin yerleşik Visual Studio tümleştirmesiyle).

  - Unity için Visual Studio Araçları, yalnızca Visual Studio 2015 + ' u destekleyecektir.

  - Eski dil hizmeti, hata listesi ve durum çubuğu kaldırıldı.

  - Hızlı Monodavranış Sihirbazı kaldırıldı (adanmış IntelliSense desteğinin yararına).

## <a name="3903"></a>3.9.0.3

Yayın Tarihi: 28 Kasım 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Çok birinci projede bulunan betikleri eklerken veya kaldırırken düzeltilen proje yeniden yükleme ve IntelliSense sorunları.

## <a name="3902"></a>3.9.0.2

Yayın Tarihi: 19 Kasım 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Visual Studio veya Unity, özellikle 'Unity İşleme İliştir' ulaşmaktan olduğunda dondurma yapma veya oyunu yeniden Unity'nın hata ayıklayıcısı altyapısı ile iletişim kurmak için kullanılan Kitaplığı'nda bir kilitlenme düzeltildi.

## <a name="3901"></a>3.9.0.1

15 Kasım 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Başka bir varsayılan düzenleyici seçildiğinde sabit Unity eklentisini etkinleştirme.

## <a name="3900"></a>3.9.0.0

13 Kasım 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Unity tarafından sabit bir Unity performans hatanın geçici çözümü geri alındı.

## <a name="3807"></a>3.8.0.7

Yayın Tarihi: 20 Eylül 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - (Backported 3.9.0.2 gelen) Visual Studio veya Unity, özellikle 'Unity İşleme İliştir' ulaşmaktan olduğunda dondurma yapma veya oyunu yeniden Unity'nın hata ayıklayıcısı altyapısı ile iletişim kurmak için kullanılan Kitaplığı'nda bir kilitlenme düzeltildi.

## <a name="3806"></a>3.8.0.6

Yayın Tarihi: 27 Ağustos 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Proje ve çözüm yeniden düzeltildi.

## <a name="3805"></a>3.8.0.5

Yayın Tarihi: 20 Ağustos 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Abonelik elden izleme sabit bir proje.

## <a name="3804"></a>3.8.0.4

Yayın Tarihi: 14 Ağustos 2018

### <a name="new-features"></a>Yeni Özellikler

- **Değerlendirme:**

  - İşaretçi değerleri için destek eklendi.

  - Genel metotlar için desteği eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Birden çok proje ile akıllı yeniden değiştirildi.

## <a name="3803"></a>3.8.0.3

24 Temmuz 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - (Backported 3.9.0.0 gelen) Unity tarafından sabit bir Unity performans hatanın geçici çözümü geri alındı.

## <a name="3802"></a>3.8.0.2

7 Temmuz 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Unity performans hatanın geçici çözüm: projeleri oluştururken MonoIslands önbellek.

## <a name="3801"></a>3.8.0.1

26 Haziran 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Hata ayıklama:**

  - UserLog ve UserBreak komutları için destek eklendi.

  - Eklenen lazy türü yükleme desteği (Ağ Yükü ve hata ayıklayıcı yanıt gecikme süresi en iyi duruma getirme).

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - İkili-işleç ifade değerlendirmesi ve yöntem arama geliştirildi.

## <a name="3800"></a>3.8.0.0

30 Mayıs 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Hata ayıklama:**

  - Zaman uyumsuz yapılarında değişkenler görüntülemek için destek eklendi.

  - İç içe geçmiş türler derleyici yapılarıyla uyarıları önlemek için kesme noktaları, ayarlarken işlemek için destek eklendi.

- **Tümleştirme:**

  - İçin destek eklendi textmate dil bilgisi için gölgelendiriciler (C++ iş yükünde artık gölgelendirici kod coloration için gereklidir).

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Taşınabilir pdb mdb için artık yeni Unity çalışma zamanı kullanırken dönüştürmez.

## <a name="3701"></a>3.7.0.1

7 Mayıs 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Yükleyici:**

  - Deneysel kullanırken sabit bağımlılık sorun oluşturur.

## <a name="3700"></a>3.7.0.0

7 Mayıs 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Hata ayıklama:**

  - (Birden çok oyuncuların/düzenleyici ile aynı Visual Studio oturumu hata ayıklama) düzenlenmiş hata ayıklama için destek eklendi.

  - Android USB player hata ayıklama için destek eklendi.

  - UWP/ıl2cpp player hata ayıklama için destek eklendi.

- **Değerlendirme:**

  - Onaltılık tanımlayıcıları için destek eklendi.

  - Gelişmiş İzleme penceresinde değerlendirme deneyimi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Özel durum ayarları sabit kullanımı.

- **Proje oluşturma:**

  - Paket Yöneticisi derleme biriminden kuşaktan hariç tutun.

## <a name="3605"></a>3.6.0.5

13 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Yeni Proje Oluşturma Aracı'nda Unity 2018.1 desteği eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Bozuk durum özel projeler içeren işleme düzeltildi.

- **Hata Ayıklayıcı:**

  - Sonraki deyimin ayarlanması düzeltildi.

## <a name="3604"></a>3.6.0.4

5 Mart 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Mono sürüm algılama düzeltildi.

- **Tümleştirme:**

  - 2018.1 ile zamanlama sorunları düzeltildi ve eklentisini etkinleştirme.

## <a name="3603"></a>3.6.0.3

23 Şubat 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - .NET Standard için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Sabit Unity hedef framework algılama.

- **Hata Ayıklayıcı:**

  - Sabit bozucu dışında usercode attığı özel durumları hakkında.

## <a name="3602"></a>3.6.0.2

7 Şubat 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - UnityMessage API yüzeyi 2017.3 için güncelleştirin.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Yalnızca dış değişiklik (azaltma ile) projeleri yeniden yükleyin.

## <a name="3601"></a>3.6.0.1

Yayın Tarihi: 24 Ocak 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Mdb hata ayıklama sembol dönüştürme sabit otomatik pdb.

  - Dizi boyutu değiştirilmeye çalışılırken Inspector'ı etkileyen EditorPrefs.GetBool sabit dolaylı çağrı.

## <a name="3600"></a>3.6.0.0'dan

10 Ocak 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - 2018.1 MonoIsland başvuru modeli için destek eklendi.

- **Değerlendirme:**

  - $Exception tanımlayıcısı için destek eklendi.

- **Hata Ayıklayıcı:**

  - Yeni Unity çalışma zamanı ile DebuggerHidden/Debuggestepthrough öznitelikler için destek eklendi.

- **Sihirbazlar:**

  - Sihirbazlar için 'Son' sürümü tanıtır.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Oynatıcı projeleri için proje GUID hesaplama düzeltildi.

- **Hata Ayıklayıcı:**

  - Kesme olayları işleme, bir yarış düzeltildi.

- **Sihirbazlar:**

  - Roslyn bağlam yöntemi eklemeden önce yenileyin.

## <a name="3503"></a>3.5.0.3

9 Ocak 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Mdb hata ayıklama sembol dönüştürme sabit otomatik pdb.

## <a name="3502"></a>3.5.0.2

Yayın Tarihi: 4 Aralık 2017

### <a name="new-features"></a>Yeni Özellikler

- **Tümleştirme:**

  - Artık Unity'de bir betik eklediğinizde veya kaldırdığınızda Unity projeleri Visual Studio'da otomatik olarak yeniden yükleniyor.

- **Hata Ayıklayıcı:**

  - Unity Editor'daki hata ayıklama için Mac için Visual Studio ve Xamarin tarafından paylaşılan Mono hata ayıklayıcısını kullanma seçeneği eklendi.

  - Taşınabilir hata ayıklama sembol dosyaları için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Tümleştirme:**

  - Kurulum bağımlılıkları sorunlar düzeltildi.

  - Sabit Unity API Yardım menüsü gösterilmiyor.

- **Proje oluşturma:**

  - Sabit player proje oluşturma ıl2cpp/.NET 4.6 arka ucu ile bir UWP oyunu üzerinde çalışırken.

  - Ek .dll uzantısı yanlış derleme dosya adına eklenmiş düzeltildi.

  - Belirli bir proje API uyumluluk düzeyi yerine genel bir sabit kullanımı.

  - Varsayılan 'true' olduğunda AllowAttachedDebuggingOfEditor Unity bayrağı zorlamaz.

## <a name="3402"></a>3.4.0.2

Yayın Tarihi: 19 Eylül 2017

### <a name="new-features"></a>Yeni Özellikler

- **Proje oluşturma:**

  - Assembly.json derleme birimler için destek eklendi.

  - Unity derlemeleri proje klasörüne kopyalama durduruldu.

- **Hata Ayıklayıcı:**

  - Yeni Unity çalışma zamanı ile sonraki deyimi ayarlamak için destek eklendi.

  - Decimal türü ile yeni Unity çalışma zamanı desteği eklendi.

  - Örtük/açık dönüştürmeler için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - Dizi oluşturma örtük boyutu sabit.

  - Sabit derleyici Yereller öğeleriyle oluşturulur.

- **Proje oluşturma:**

  - Microsoft.CSharp sabit başvuru için 4,6 API düzeyi.

## <a name="3302"></a>3.3.0.2

Yayın Tarihi: 15 Ağustos 2017

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Visual Studio çözümü oluşturma Unity 5.5 ve önceki sürümlerde düzeltildi.

## <a name="3300"></a>3.3.0.0

Yayın Tarihi: 14 Ağustos 2017

### <a name="new-features"></a>Yeni Özellikler

- **Değerlendirme:**

  - Yapılar yeni Unity çalışma zamanı ile oluşturma desteği eklendi.

  - İşaretçileri minimalist desteği eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Değerlendirme:**

  - Fixed yöntemi çağırma temelleri üzerinde.

  - Alan değerlendirme Beforefiledinit ile işaretlenen türlerdeki ile düzeltildi.

  - İkili işleçli (çıkar) sabit olmayan desteklenen çağırır.

  - Visual Studio saate öğeleri eklerken sorunlar düzeltildi.

- **Proje oluşturma:**

  - Derleme adı başvuruları mcs.rsp dosyalarıyla düzeltildi.

  - Sabit ile API düzeyleri tanımlar.

## <a name="3200"></a>3.2.0.0

Yayın Tarihi: 10 Mayıs 2017

### <a name="new-features"></a>Yeni Özellikler

- **Yükleyici:**

  - MEF önbelleği temizleme desteği eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Kod Düzenleyicisi:**

  - Sabit sınıflandırma/tamamlama özel özniteliklere sahip.

  - Unity iletileri ile titremeyi düzeltildi.

## <a name="3100"></a>3.1.0.0

Yayın Tarihi: 7 Nisan 2017

### <a name="new-features"></a>Yeni Özellikler

- **Hata Ayıklayıcı:**

  - Yeni Unity çalışma zamanı desteği eklendi (.NET 4.6 ile / C# 6 uyumluluğu).

- **Proje oluşturma:**

  - .NET 4.6 profili için destek eklendi.

  - Mcs.rsp dosyaları için destek eklendi.

  - Unity 5.6 kullanıldığında her zaman güvensiz derleme anahtar etkinleştirin.

  - "Player" proje oluşturma desteği eklendi Windows Store platform ve ıl2cpp arka ucu kullanırken.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Kod Düzenleyicisi:**

  - Giriş işareti konumunu, otomatik tamamlama yöntemi ekledikten sonra düzeltildi.

- **Proje oluşturma:**

  - Kaldırılan derleme sonrası işleme sürümü.

## <a name="3001"></a>3.0.0.1

Yayın Tarihi: 7 Mart 2017

### <a name="this-version-includes-all-new-features-and-bug-fixes-introduced-with-28x-series"></a>Bu sürümü, tüm yeni özellikler ve hata düzeltmeleri 2.8.x serisi ile sunulan içerir.

## <a name="2820---30-preview-3"></a>2.8.2.0 - 3.0 preview 3
25 Ocak 2017 tarihinde yayımlandı

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - Burada eklenti projeleri iki kez başvurulan burada ilk olarak ikili bir DLL sonra bir proje olarak başvuruda gerilemesi düzeltildi.

## <a name="2810---30-preview-2"></a>2.8.1.0 - 3.0 Önizleme 2
Yayın Tarihi: 23 Ocak 2017

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Kod Düzenleyicisi:**

  - Bir öznitelik bildirimi olmadan küme ayracı tamamlama başlatırken bir kilitlenme düzeltildi.

- **Hata Ayıklayıcı:**

  - Eş yordamlar yeni Unity derleyici/çalışma zamanı altında sabit bir işlev kesme noktaları.

  - Eklenen uyarı durumunda (karşılık gelen kaynak konumu bulunduğunda) unbindable bir kesme noktası.

- **Proje oluşturma:**

  - Özel ve yerelleştirilmiş karakterleri ile csproj oluşturma düzeltildi.

  - Sabit başvuruları kitaplığı (gibi Facebook SDK'sı) gibi varlıkları dışında.

- **Çeşitli:**

  - Unity yüklemeden veya kaldırmadan olduğunda çalışmasını engellemek için bir denetim eklendi.

  - Uzak Unity belgeleri hedeflemek için https olarak değiştirdi.

## <a name="2800---30-preview"></a>2.8.0.0 - 3.0 Önizleme
17 Kasım 2016 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- **Genel:**

  - Visual Studio 2017 yükleyicisi desteği eklendi.

  - Visual Studio 2017 uzantısı desteği eklendi.

  - Eklenen yerelleştirme desteği.

- **Kod Düzenleyicisi:**

  - Ek C# Unity iletileri için IntelliSense.

  - Ek C# kod coloration Unity iletileri için.

- **Hata Ayıklayıcı:**

  - İçin destek eklendi `is`, `as`, doğrudan tür dönüştürme; `default`, `new` ifadeler.

  - Dize concat ifadeleri için destek eklendi.

  - Onaltılık gösterim tamsayı değerleri için destek eklendi.

  - Yeni geçici değişkenlerin (ifadeler) oluşturma desteği eklendi.

  - Temel örtülü dönüştürmeler için destek eklendi.

  - Daha iyi bir tür bekleniyor veya nebyl nalezen hata iletileri eklendi.

- **Proje oluşturma:**

  - CSharp soneki proje adlarından kaldırıldı.

  - Bir sistem geniş msbuild hedef dosyası kaldırılan başvuru.

- **Sihirbazlar:**

  - Düzenleyici veya EditorWindow gibi olmayan davranışı türlerinde Unity iletileri için destek eklendi.

  - Ekleme ve Unity iletileri için Roslyn değiştirdi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Hata Ayıklayıcı:**

  - Genel türler değerlendirirken Unity kilitlenme düzeltildi.

  - Boş değer atanabilir türler sabit işlenmesi.

  - Numaralandırmalar sabit işlenmesi.

  - İç içe üyesi türlerin sabit işleme.

  - Sabit koleksiyonu dizin oluşturucusu erişim.

  - Sabit yineleyici çerçeve yeni C# derleyicisi ile hata ayıklama desteği.

- **Proje oluşturma:**

  - Unity Web Oynatıcısı hedeflenirken derleme önleyen hata düzeltildi.

  - Bir web ile bir komut dosyası derlenirken derleme önleyen hata düzeltildi, dosya adı kodlanmış.

## <a name="2300"></a>2.3.0.0

Yayınlanma tarihi: 14 Temmuz 2016

### <a name="new-features"></a>Yeni Özellikler

- **Genel:**

  - Visual Studio hata listesinde Unity konsolundan devre dışı bırakmak için bir seçenek günlükleri eklendi.

  - Oluşturulan proje özellikleri değiştirilmesine izin verme seçeneği eklendi.

- **Hata Ayıklayıcı:**

  - Eklenen metin, XML, HTML ve JSON görselleştiriciler dize.

- **Sihirbazlar:**

  - MonoBehaviors eksik eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Genel:**

  - Denetim içinde görüntülenmesini Visual Studio ayarları önleyen ReSharper ile bir çakışma çözüldü.

  - Bazı durumlarda hata ayıklamayı engelleyen Xamarin ile bir çakışma çözüldü.

- **Hata Ayıklayıcı:**

  - Visual Studio'nun hata ayıklama sırasında donmasıyla sonuçlanabiliyor nedeni bir sorun düzeltildi.

  - Visual Studio 2015'te işlev kesme noktaları ile bir sorun düzeltildi.

  - Birden fazla ifade değerlendirme sorunları düzeltildi.

## <a name="2200"></a>2.2.0.0

Yayınlanma tarihi: 4 Şubat 2016

### <a name="new-features"></a>Yeni Özellikler

- **Sihirbazlar:**

  - Eklenen akıllı arama **uygulama MonoBehavior** Sihirbazı.

  - Yapılan sihirbazları bağlamı kullanan; Örneğin, NetworkBehavior iletileri yalnızca bir NetworkBehavior ile çalışırken kullanılabilir.

  - Sihirbazlar NetworkBehavior iletiler için destek eklendi.

- **UI:**

  - MonoBehavior iletilerin görünürlüğünü yapılandırmak için bir seçenek eklenmiştir.

  - Visual Studio için Unity projeleri ilgili olmayan özellik sayfalarını kaldırıldı.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Proje oluşturma:**

  - UnityEngine ve Unity 4.6 üzerinde UnityEditor sabit başvuruları.

  - Sabit Unity OSX üzerinde çalışırken proje dosyalarının oluşturulmasını.

  - Proje adları hashmark (#) karakterleri içeren sabit işlenmesi.

  - Oluşturulan projeleri C# 4'e sınırlı.

- **Hata Ayıklayıcı:**

  - Bir sorun, bir Unity eş yordam içinde hata ayıklama sırasında ifade değerlendirme ile düzeltildi.

  - Visual Studio'nun hata ayıklama sırasında donmasıyla sonuçlanabiliyor nedeni bir sorun düzeltildi.

- **UI:**

  - Bir uyumsuzluk sabit [sekmeleri Studio](https://tabsstudio.com/) Visual Studio uzantısı.

- **Yükleyici:**

  - HKLM Kayıt defteri girişleri oluşturarak VSTU (tüm kullanıcılar için yüklenir) makineye yüklenmesini destekler.

  - Visual Studio'nun birden çok farklı sürümleri için VSTU sürümüyle aynı sürümü yüklendiğinde VSTU kaldırılması ile sorunlar düzeltildi. Örneğin, VSTU **2015** 2.1.0.0 ve VSTU **2013** 2.1.0.0 hem takıldı.

## <a name="2100"></a>2.1.0.0

8 Eylül 2015'i yayınladı

### <a name="new-features"></a>Yeni Özellikler

- Unity 5.2 için destek

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Unity üzerinde menü öğeleri görüntüle < 4.2

- Bir hata iletisi artık Visual Studio XML IntelliSense dosyalarını kilitler görüntülenir.

- Tanıtıcı <\<sorunu gidermeye çalışırken değiştirdiği >> koşullu bağımsız değişkeni bir boolean değeri değil, koşullu kesme noktaları.

- Windows Store uygulamaları için UnityEngine ve UnityEditor derlemelere başvuruları sabit.

- Hata ayıklayıcıda adımla düzeltilen hata: Adım, genel özel durum.

- Visual Studio 2015'te sabit isabet sayısı kesme noktaları.

## <a name="2000"></a>2.0.0.0

20 Temmuz 2015'i yayınladı

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Unity tümleştirmesi:**

  - Bir DLL ve onun hata ayıklama simgeleri (PDB) içeri aktarırken Visual Studio 2015 ile oluşturulan hata ayıklama sembolleri dönüştürme sabit.

  - Her zaman MDB dosyaları bir DLL ve onun hata ayıklama simgeleri (PDB) içeri aktarılırken ne zaman bir MDB dosyası ayrıca sağlanan dışında oluşturun.

  - Sabit kirlilik Unity proje dizininin obj dizinine sahip.

  - Başvuruları System.Xml.Link ve System.Runtime.Serialization sabit oluşturma.

  - Kancaları. birden fazla aboneye proje dosyası oluşturma API desteği eklendi.

  - Oluşturulacak dosyalardan biri kilitli olduğunda bile her zaman tam proje dosyası oluşturma.

  - İçin destek eklendi * uzantı joker karakter filtre belirtmek için C# projesinde dahil edilecek dosyalar.

- **Visual Studio tümleştirmesi:**

  - Productivity Power Tools ile bir uyumluluk sorunu düzeltildi.

  - Olaylar ve temsilciler bildirimleri MonoBehaviors oluşturma düzeltildi.

- **Hata Ayıklayıcı:**

  - Hata ayıklama sırasında olası dondurma düzeltildi.

  - Burada Yereller belirli yığın çerçevelerinde görüntülenmez bir sorun düzeltildi.

  - Boş bir dizi inceleyerek düzeltildi.

## <a name="1990---20-preview-2"></a>1.9.9.0 - 2.0 preview 2
2 Nisan 2015'i yayınladı

### <a name="new-features"></a>Yeni Özellikler

- **Unity Proje Gezgini:**

  - Unity proje Gezgininde dosya yeniden adlandırılırken, sınıf otomatik olarak yeniden adlandırın (bkz **seçenekleri** iletişim).

  - Otomatik olarak yeni oluşturulan betiklerini, Unity proje Gezgininde seçin.

  - Unity proje Gezgininde etkin betik izleyin (bkz **seçenekleri** iletişim).

  - Visual Studio Çözüm Gezgini'nde çift-eşitleme (bkz **seçenekleri** iletişim).

  - Unity proje Gezgininde Visual Studio simgeler benimseyin.

- **Hata Ayıklayıcı:**

  - Etkin hata ayıklama hedefi kaydedilmiş veya yakın zamanda kullanılan hata ayıklama hedefleri listesinden seçin (bkz **seçenekleri** iletişim).

  - İşlev kesme noktaları MonoBehavior yöntemlerde oluşturabilir ve bunları birden çok MonoBehavior sınıflarına uygulayabilirsiniz.

  - Nesne Kimliği yap hata ayıklayıcıda destekler.

  - Destek kesme noktası isabet sayısı hata ayıklayıcısı.

  - (Deneysel. hata ayıklayıcıda kesme üzerinde özel durum desteği Bkz: **seçenekleri** iletişim).

  - Hata ayıklayıcıdaki ifadeler değerlendirildiğinde nesneler ve diziler oluşturulmasını destekler.

  - Null karşılaştırma desteği, Hata ayıklayıcıdaki ifadeler değerlendirme.

  - Eski üyeler hata ayıklayıcı gözlem pencerelerinde filtreleyin.

- **Yükleyici:**

  - En iyi duruma getirilmiş Visual Studio Araçları için Unity uzantısı kaydı.

  - Visual Studio Araçları için Unity 5 için Unity paketini yükleyin.

- **Belgelerle** Belge oluşturma performansını geliştirir.

- **Sihirbazlar:** Unity 4,6 ve Unity 5 için yeni MonoBehavior yöntemlerini destekler.

- **Unity:** Proje dosyası oluşturma sırasında. rsp dosyalarında güvenli olmayan bayraklar ve özel tanımlar arama yapın.

- **UI:** Visual Studio 'da Unity için Visual Studio Araçları **seçenekleri** iletişim kutusu eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- **Unity Proje Gezgini:**

  - Taşınmış ya da Visual Studio Çözüm Gezgini'nden yeniden adlandırılmış dosyaları sonra Unity proje Gezgini'ni yenileyin.

  - Unity proje Gezgininde dosya yeniden adlandırılırken seçimleri koruyun.

  - Otomatik önlemek genişletip Unity proje Gezgininde tıkladı dosyaları çift olduğunda daraltabilirsiniz.

  - Yeni seçilen dosyaları Unity proje Gezgininde görünür olduğundan emin olun.

- **Hata Ayıklayıcı:**

  - Visual Studio Hata ayıklayıcıdaki ifadeler değerlendirildiğinde dondurma olası engelleme.

  - Yöntem çağrıları hata ayıklayıcısı doğru etki alanında olması emin olun.

- **Unity:**

  - Unity 5 UnityVS.OpenFile konumunu düzeltin.

  - Unity 5 pdb2mdb konumunu düzeltin.

  - Proje dosyası oluşturma sırasında olası bir özel durumu engellersiniz.

  - Unity OSX üzerinde çalışırken olası dondurma engelleyin.

  - İç özel durumları işler.

  - İçin VS hata listesi Unity konsol günlükleri gönderin.

- **Belgelerle** Yeni Unity belgeleri için doğru belge oluşturma.

- **Proje** Gerektiğinde de Unity. meta dosyalarını taşıyın ve yeniden adlandırın.

- **Sihirbazlar:** Kod oluştururken MonoBehavior yöntem parametrelerinin sırasını düzeltin.

- **UI:** Bağlam menüsü ve simgeler için Visual Studio temalarını destekleme.

## <a name="1980---20-preview"></a>1.9.8.0 - 2.0 Önizlemesi
12 Kasım 2014'te yayımlamıştır

### <a name="new-features"></a>Yeni Özellikler

- Visual Studio 2015 için destek.

- Visual Studio 2015'te Unity gölgelendiriciler için kod Coloration.

- Geliştirilmiş görsel olarak hata ayıklama sırasında değerleri:

  - Daha iyi görselleştirme ArrayLists, listeler, Hashtable'da ve sözlük.

  - Genel olmayan üyeler ve statik üyeler İzlemedeki ve yerel görünümlerle kategorileri gösterme.

  - Unity'nın SerializedProperty yalnızca özellik için geçerli bir değer alanı değerlendirmek için geliştirilmiş görüntüsü.

  - Sınıflar ve yapılar DebuggerDisplayAttribute desteği.

  - DebuggerTypeProxyAttribute desteği.

- Kodlama kuralları kullanıcı cevaben bizim sihirbazları kullanarak MonoBehaviour yöntemleri ekleme yapın.

- UnityVS oluşturulan projeleri derleme zamanı metin şablonları için destek uygular.

- ResX kaynakları için destek oluşturulan UnityVS projelerinde uygulayın.

- Unity Visual Studio'dan gölgelendiricileri açma desteği.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- İliştirme işleminden sonra Unity oyun başlatmadan önce yuvaların ve Visual Studio'da Play tetiklendi. Bu bazı sorunlar ile Unity VS arasında bağlantı kararlılığını İliştir ve Yürüt kullanırken düzeltir.

- Unity'nın komut dosyası altyapısı hata ayıklayıcı arabiriminde Unity dondurulamıyor meyillidir yöntemleri çağırmaktan kaçının. Bu, hata ayıklayıcı eklerken Unity dondurma düzeltir.

- Sembol kullanılabilir olduğunda çağrı yığınını görüntüleme düzeltin.

- İçin yoksa, günlük geri kaydetmeyin.

## <a name="1920"></a>1.9.2.0

9 Ekim 2014'te yayımlamıştır

### <a name="new-features"></a>Yeni Özellikler

- Unity oyuncuların algılanması geliştirin.

- Bizim dosya açan kullanırken, dosya adının yanı sıra, satır numarası geçirmek Unity olun.

- Çevrimiçi Unity belgeleri için varsayılan olarak yerel bir belge yok ise.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Bir etki alanı yeniden sonra bir kesme noktasına ulaşma olası Unity kilitlenme düzeltildi.

- Bizim yapılandırma kapatırken Unity konsolunda gösterilen özel durumları düzeltin veya windows hakkında bir etki alanı sonra yeniden yükleyin.

- Yerel olarak çalışan 64 bit Unity algılanması düzeltin.

- Sihirbazlar Unity sürümünde her Monobehaviour filtreleme düzeltin.

- Burada uzantı filtresi boşsa tüm varlıkları proje dosyalarında bulunan hatası düzeltildi.

## <a name="1910"></a>1.9.1.0

22 Eylül 2014'te yayımlamıştır

### <a name="new-features"></a>Yeni Özellikler

- Bağlama kesme noktası için kaynak konumları iyileştirin.

- Hata ayıklayıcı ifade değerlendirmesindeki aşırı yüklenmiş yöntemler için destek.

- Kutulama temelleri ve hata ayıklayıcı ifade değerlendirmesindeki değer türleri için destek.

- Anonim yöntemler hata ayıklama sırasında C# yerel değişkenler ortamın oluşturulması destekler.

- Silin ve Visual Studio'dan dosyaları yeniden adlandırma veya silme .meta dosyalarını yeniden adlandırın.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Visual Studio temasından işlenmesini düzeltin. Daha önce siyah Temalar iletişim kutuları boş görünebilir.

- Unity dondurma Unity yeniden derlenmesi sırasında hata ayıklayıcı bağlanırken, düzeltmek.

- Uzak düzenleyiciler veya başka bir sistem üzerinde derlenmiş oyuncuların hata ayıklanırken kesme noktaları düzeltin.

- Bir kesme noktası isabet edildiğinde olası bir Visual Studio kilitlenme sorunu düzeltildi.

- Kesme noktaları olarak gösteren önlemek için bağlama düzeltme kesme noktaları kaldırıldı.

- Kapsam dışına görüntülenen dinamik değişkenleri önlemek için hata ayıklayıcı değişken kapsamı işlenmesini düzeltin.

- Statik üyeleri arama ifade değerlendirmesinde hata ayıklayıcı düzeltin.

- Statik alanlar ve Özellikler göstermek için hata ayıklayıcı ifade değerlendirmesindeki türlerini görüntüleme düzeltin.

- Unity proje adları Visual Studio'nın (Connect sorun #948666) engelliyor özel karakterler içerdiğinde çözüm oluşturulmasını düzeltme.

- Unchecked (Connect sorun #933357) seçeneğini sonra konsol olay göndermeye hemen durdurmak için Visual Studio Araçları Unity paketini düzeltin.

- Başvurular düzgün UnityEngine.UI gibi yeni API'ler başvuruları UnityVS oluşturulan projelerde yeniden algılanması düzeltin.

- Yükleyici bozuk yüklemeleri önlemek için yüklemeden önce Visual Studio kapalı olduğunu gerektirecek şekilde düzeltin.

- VSTU tüm sürümleri arasında paylaşılan bir uygun bir tek başına bileşeni Unity başvuru derlemelerini yüklemek için yükleyici düzeltin.

- Betikleri açma VSTU ile Unity 64 bit sürümlerinde düzeltin.

## <a name="1900"></a>1.9.0.0

29 Temmuz 2014'te yayımlamıştır

### <a name="new-features"></a>Yeni Özellikler

- Unity hata ayıklayıcı Ekle penceresinde, bir özel IP ve bağlantı noktası hata ayıklamak için girin olanağı eklendi.

- Arka planda çalışıp için Unity ayarlamak için yapılandırma seçeneği ekleyin.

- Çözüm ve proje dosyaları ya da yalnızca proje dosyaları oluşturmak için yapılandırma seçeneği ekleyin.

- Başlangıç hedef: Unity Ekle veya Unity ve Play Ekle öğesini seçin.

- Çok boyutlu diziler hata ayıklayıcı görüntü.

- Yeni Unity Player'da hata ayıklama bağlantı noktalarını işler.

- Unity'nün 4.6 GUI derlemeleri gibi yeni Unity derlemelere başvuruları işleyin.

- Hata ayıklarken yerel değişkenler düzgün görüntülenmesi için kapanışlar deconstructs.

- Oluşturulan Yineleyicilerin değişkenleri, hata ayıklama sırasında bağımsız değişkenleriyle deconstructs.

- Bir projeyi yeniden sonra Unity Proje Gezgini'nın durumu korur.

- Unity Proje Gezgini geçerli belge ile eşitlemek için bir komut ekleyin.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Koşullu kesme noktaları hata ayıklayıcıyı başlatmadan önce koşulları ayarlayın düzeltin.

- UnityEngine uyarılarından kaçınmak için başvurular düzeltin.

- Unity betalar için ayrıştırma sürümleri düzeltin.

- Burada değişkenler yerel değişkenler penceresinde bir kesme noktasına ulaşma olduğunda gösterilmeyebiliyor sorunu düzeltin veya Adımlama.

- Değişkenleri araç ipuçları, Visual Studio 2013'te düzeltin.

- Unity 4.5 IntelliSense belgelerini oluşturulmasını düzeltme.

- Unity düzeltme / bir etki alanından sonra Visual Studio iletişim (play/stop Unity) yeniden yükleyin.

- Visual Studio temasından bölümlerini işlenmesini düzeltin.

> [!IMPORTANT]
> C# Unity ekosisteminde - yeni örnek varlıkları hakim dili olan C# ' de, Unity belgeleri varsayılan C# - C# deneyimi daha fazla odaklanması UnityScript ve hata için temel destek kaldırdık. Sonuç olarak, VSTU çözümleri artık yalnızca C# değildir ve yüklemek için daha hızlıdır.

## <a name="1820"></a>1.8.2.0

7 Ocak 2014'te yayımlamıştır

### <a name="new-features"></a>Yeni Özellikler

- Unity'nın komut dosyası altyapısının ağ katmanında bir soruna geçici bir çözüm üzerinde Mavericks düzenleyicileri uzak bulma için çalışır.

- Uzak Unity oyuncuların bulmak için yeni bağlantı noktaları işleyin.

- Hedef yapı geçerli belirli UnityEngine bütünleştirilmiş kod başvurusu.

- Oluşturulan projeleri içerecek şekilde filtre dosyalara ayarı ekleyin.

- Visual Studio hata listesi gönderen konsol günlüklerine devre dışı bırakma ayarı ekleyin. Nedeni olarak yalnızca bir geri çağırma konsol günlükleri almak için Unity içinde kayıtlı PlayMaker veya konsol Pro kullanıyorsanız, bu yararlıdır.

- Mdb hata ayıklama sembolleri oluşturmayı devre dışı bırakma ayarı ekleyin. Kendiniz mdb oluşturma, bu yararlıdır.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Unity VS'den açılmış dosyalar bir gerileme düzeltildi > = 4.2 IntelliSense kaybeder.

- Özel Temalar işlemek için sunduğumuz VS iletişim kutuları düzeltin.

- Bağlam menüsüne UPE kapatma düzeltin.

- Unity kilitlenme eşitlenmemiş, derleme sürüm özel oluşturulmuş engelleyin.

## <a name="1810"></a>1.8.1.0

Yayımlanan 21 Kasım 2013

### <a name="new-features"></a>Yeni Özellikler

- MonoBehaviour sihirbazları Unity 4.3 API'leri ile ayarlanır.

- MonoBehaviour sihirbazları Unity API'leri sürüme bağlı olarak filtre.

- System.Xml.Linq başvuru için Unity projeleri Ekle > 4.1.

- Stacktrace başına iletisinde içermeyecek şekilde Debug.Log bizim çağrısına prettify.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Burada şu JavaScript dosyaları Visual Studio'da varsayılan işleme ile neden bir hata düzeltildi.

- Bu süre içinde VS, gerçek görünen bir beyaz piksel düzeltildi.

- Sabit bir SCM tarafından salt okunur olarak işaretlenmiş olması durumunda UnityVS.VersionSpecific derlemeyi silme işlemi.

- Yuva UnityVS paketi oluştururken sabit özel durumlar.

- Visual Studio derlemelerden stok görüntüleri yüklenirken Visual Studio'da bir kilitlenme sorunu düzeltildi.

- Unity derlemeleri kaynak UnityVS.VersionSpecific oluşturulmasında içinde bir hata düzeltildi.

- Bir yuva Unity pakette açılırken olası dondurma düzeltildi.

- Unity proje bir tire (-) ile işlenmesini adında düzeltildi.

- ALT + sekme sırasını Unity 4.2 ve üzeri karıştırmamaya Unity'de açılış betikleri düzeltildi.

## <a name="1800"></a>1.8.0.0

24 Eylül 2013 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Hata ayıklayıcı bağlantı hızını önemli ölçüde geliştirildi.

- Dosya ve satır Unity 4.2 ve üzeri için Gezinti otomatik olarak işler.

- Koşullu kesme noktaları.

- Proje dosya oluşturucu artık T4 şablonlarını işler.

- MonBehavior sihirbazları yeni API'ler ile güncelleştirin.

- C# IntelliSense belgelerini Unity türleri için.

- Aritmetik ve mantıksal ifadeleri değerlendirme.

- Uzaktan hata ayıklama preview için Uzak düzenleyicileri daha iyi bulma.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Biz burada sızıntı bir iş parçacığı VS hata ayıklayıcı bağlantısını kestikten sonra düzeltildi.

- VS'de görünen bir beyaz piksel düzeltildi.

- Durum çubuğu simgesine tıklama işleme düzeltildi.

- Eklentileri klasörlerdeki derlemeleri ile başvuruları nesil düzeltildi.

- Yuva özel durumları durumunda UnityVS paketinden sabit oluşturma.

- Yeni sürümlerini UnityVS algılanması düzeltildi.

- Lisans süresi dolduğunda Lisans Yöneticisi'nin istemi düzeltildi.

- İşlem listesi boş VS işlem penceresi için ek hata ayıklayıcı işleme bir hata düzeltildi.

- Yerel görünümünde Boole değerleri, sabit değişen değerler.

## <a name="1220"></a>1.2.2.0

9 Temmuz 2013 yayımlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- İfade değerlendirici tam adlarını işleyin.

- Özel durum işleme için ilgili bir dondurma burada Unity komut dosyası altyapısı bize yanlış stackframe veri gönderiyor düzeltildi.

- Web hedefler için derleme işlemi düzeltildi.

- Visual Studio başlatıldığından ve silinen bir dosyayı başlangıçta açmak için dosya listesi olduğu meydana gelmiş olabilir bir hata düzeltildi.

- Benzer olmayan komut dosyalarını işlemek için sabit UnityVS.OpenFile gölgelendiricileri derlenmiş.

- Biz artık Boo.Lang ve UnityScript.Lang tüm C# içinden projeleri başvuru.

- Proje özel karakterler varsa projelerinde başvuruları sabit oluşturma.

- Yöntem çağrıları için projeleri burada elden geçici bir VS sorunu birden çok NullReferenceException MessageBox tetikleyecektir.

- Unity 4.2 Beta derlemelerin sabit işleme.

## <a name="1210"></a>1.2.1.0

Yayımlanan 9 Nisan 2013

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Unity derlemeleri için kod tamamlama g/ç hatası durumunda yerel dağıtımını sabit (salt okunur dosyaları gibi veya Visual Studio tarafından kilitlenmiş dosyaları).

- Visual Studio'da zaten açıldıysa burada Unity'de bir betiğin açılması dosya odaklanmak değil bir gerileme düzeltildi.

- Yeni özel durum işleme performans sorunu düzeltildi.

- Sabit bağlama dış bazı DLL'lerde kesme noktaları.

## <a name="1200"></a>1.2.0.0

Yayımlanan 25 Mart 2013

### <a name="new-features"></a>Yeni Özellikler

- Hata ayıklayıcı bağlantı hızını önemli ölçüde geliştirildi.

- Daha büyük projeler için en iyi duruma getirilmiş Unity Proje Gezgini.

- (Veya etkinleştirmezsiniz) ayırmak için Visual Studio ayarları dikkate işlenen ve işlenmeyen özel durumlar.

- ToString yerel değişkenlerde çağırmak için Visual Studio ayarı oluşuyor.

- Ekleme yeni menü hata ayıklama -> Unity oyuncuların hata ayıklamak için kullanabileceğiniz ekleme Unity hata ayıklayıcı.

- Çözüm dosyası oluşturma sırasında UnityVS çözüm eklenen özel projeler korur.

- Ekleme yeni klavye kısayolu CTRL + ALT + M, giriş işareti konumuna Unity işlevi veya üye için Unity belgeleri görüntülemek için CTRL + H ->.

- Derleyici yanıt dosyaları (rsp), Visual Studio ile derleme yapılırken dikkate alın.

- Oluşturucu yöntemleri hata ayıklama sırasında değişkenleri göstermek için derleyicinin ürettiği türleri ayrıştırma.

- Uzak bir paylaşılan klasöre Unity yapılandırma gereksinimini ortadan kaldırarak hata ayıklama basitleştirin. Şimdi Windows için Unity projeniz erişimi yeterlidir.

- Özel Unity profil, bir standart .net hedef profil yükleyin. Bu, ReSharper gösterebilirsiniz tüm hatalı pozitif sonuçları düzeltir.

- Geçici bir Unity altyapısı hata, hata ayıklayıcı olmayan düzgün bir şekilde kesme olmaz şekilde komut iş parçacığı kayıtlı.

- Burada dosya açık istekte kilitlenme sırasında dosyaları açmak için talep vs'de bir yarış durumu önlemek için dosyayı açan yeniden.

- UnityVS VS oluşturulurken proje oluşturma yenilemek şimdi isteyen ve değil dosya artık kaydedin.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Sabit özel bizim .net profili

- Tema oluşturma tümleştirme sabit, bu VS 2012 koyu tema ile bizim sorunları giderir.

- VS 2012'de sabit hızlı davranışı kısayol.

- Hata ayıklama sırasında gerçekleşebilir Adımlama bir sorun düzeltildi ve ana olmayan iş parçacığı bir kesme noktasına ulaşılmasına neden olur.

- Tür diğer adları gibi tamsayı sabit UnityScript ve hata tamamlama

- Yeni UnityScript veya hata dize yazarken sabit özel durum.

- Bir çözümü yüklenmedi, Unity menüleri sabit durumlar.

- Hata düzeltildi UV'leri 48: çift tırnak bazen hataya yazıp tüm işlevi (kod tamamlama, sözdizimi vurgulama vs.) Kes.

- Düzeltilen hata UVS-46: Visual Studio 'nun Hata Listesi tıklarken yinelenen açılan betik dosyası (UnityScript).

- Düzeltilen hata UVS-42: Durum çubuğundaki Unity bağlantı logosu, VS 2012 ' deki fare olaylarını işlemez.

- Düzeltilen hata UVS-44: CTRL + SHIFT + Q, VS 2012 ' de hızlı MonoBehaviours için kullanılamaz.

- Düzeltilen hata UVS-40: VS2012 "koyu" temasından pencere etkin olmadığında Unity proje Gezgininde seçilen öğeler okunamaz.

- Düzeltilen hata UVS-39: Atlanan dizeleri simgeleştirirken sorun.

- Düzeltilen hata UVS-35: Değişkenler incelenirken nesneler üzerinde ToString öğesini çağır.

- Sabit hata UVS-27: VS2012 içinde "koyu" temayla sembol penceresi tutarsızlığına git.

- Sabit hata UVS-11: Eş öğelerdeki Yereller.

## <a name="1100---beta-release"></a>1.1.0.0 - beta sürümü
Yayımlanan, 9 Mart 2013

## <a name="10130"></a>1.0.13.0
Yayımlanan Ocak 21 Şubat 2013

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Geçersiz iş parçacığı olayları hedef hata ayıklanan gönderiyorsa, meydana gelmiş olabilir bir Visual Studio kilitleniyor düzeltildi. Bu genellikle, uzak bir Unity OSX üzerinde hata ayıklama olacağını.

- Bir özel durum hata ayıklayıcı kapanıyorsa gerçekleşebilir, Visual Studio kilitleniyor düzeltildi.

- Bir C# MonoBehavior bir ad alanında olduğunda, bizim MonoBehavior Yardımcıları düzeltildi.

- Visual Studio 2012'de UnityScript için sabit bir hata ayıklayıcı araç ipuçları.

- Yalnızca hata ayıklama sabitleri Unity'de değiştiği proje oluşturma düzeltildi.

- Unity Proje Gezgini sabit klavye gezintisi.

- Kaçış dizileri için sabit UnityScript renklendirme.

- Proje adı Unity dışında kullanıldığında daha iyi tahmin bizim dosya açan düzeltildi. Kullanıcı, bir üçüncü bölümü dosya açan temsilciler için UnityVS, Unity kullandığında, gereklidir.

- Sabit işleme için UnityVS Unity'de gönderilen uzun iletisi. Bundan önce uzun iletileri UnityVS Mesajlaşma bizim parçası kilitlenebiliyordu. Sonuç olarak, bazen UnityVS dosya Unity'de açın mıydı.

## <a name="10120"></a>1.0.12.0
3 Ocak 2013'ün yayımlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Visual Studio bir kesme noktası silerken, oluşabilir sabit Visual Studio kilitleniyor.

- Unity oyun betikleri yeniden derlenen sonra nerede bazı kesme noktaları isabet değil, bir hata düzeltildi.

- Hata ayıklayıcı kesme noktaları ilişkisiz Visual Studio doğru şekilde bildirmek için düzeltildi.

- Yerel programlarda hata ayıklamak için Visual Studio hata ayıklayıcısını engelleyen bir kayıt sorun düzeltildi.

- UnityScript değerlendirirken gerçekleşir ve ifadeleri önyük özel durum düzeltildi.

- Burada .net API düzeyini Unity proje dosyalarının bir güncelleştirme tetikleyecek değil bir gerileme düzeltildi.

- Burada kullanıcı kodu içinde günlük geri çağırma işleyiciyi katılmamayı bir API sorun düzeltildi.

## <a name="10110"></a>1.0.11.0
28 Kasım 2012 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Unity 4 resmi desteği.

- Unity Proje Gezgini betiklerin işleme.

- Visual Studio penceresinde gitmek için tümleştirme.

- Bilgi konsol iletisi hata listesinde tıklayarak kaplamaları için bu, ilk stackframe simgelerle için ayrıştırılıyor.

- Ekleme bir [API](../cross-platform/customize-project-files-created-by-vstu.md) proje oluşturma işleminde katılmasına izin vermek için.

- Ekleme bir [API](../cross-platform/share-the-unity-log-callback-with-vstu.md) içinde LogCallback katılmasına izin vermek için.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Unity Proje Gezgini Visual Studio 2012'de, sabit regresyon arka planda.

- Tam .net Profil kullanıcılar için proje oluşturma düzeltildi.

- Web hedefinin kullanıcılar için proje oluşturma düzeltildi.

- Sabit proje oluşturma dahil etmek için hata ayıklama ve izleme derleme simgeleri Unity olarak yapar.

- Özel karakterler bizim Goto sembol penceresinde kullanırken sabit kilitlenme.

- Size sunduğumuz simgesi Visual Studio durum çubuğunda eklenemiyor, sabit kilitlenme.

## <a name="10100"></a>1.0.10.0
Yayımlanan 9 Ekim 2012

### <a name="bug-fixes"></a>Hata Düzeltmeleri

- Unity Proje Gezgini arka planını Visual Studio 2010'da düzelttik.

- UnityVS, hata ayıklayıcı arabirim önceden kilitlenmiş bir Unity için hata ayıklayıcının çalıştılarsa meydana gelmiş olabilir bir Visual Studio dondurma düzeltildi.

- Bir kesme noktası ayarlandı ve AppDomain yeniden ortaya çıkabilecek meydana gelmiş olabilir bir Visual Studio dondurma düzeltildi.

- Sabit dosyalar kilitlenmesini önlemek ve Unity yapı işlemi karıştırır Unity'de derlemeleri nasıl alınır.

## <a name="1090"></a>1.0.9.0

Yayımlanan 3 Ekim 2012

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Sabit proje oluşturma, Unity projesi gerçek JavaScript varlıkları içerir.

- İfade değerlendirmesinde işleme sabit bir hata oluştu.

- Yeni değerler alanlara değer türlerinin ayarlama düzeltildi.

- Sabit olası yan kod düzenleyicisinden ifadeleri üzerine gelindiğinde etkiler.

- Sabit ifade değerlendirmesi için yüklü bütünleştirilmiş kodlarında türler nasıl aranır.

- Sabit hata UVS-21: Unity nesnelerinde atama değerlendirmesi etkisizdir.

- Sabit hata UVS-21: Unity matematik API 'sine bir yöntem çağrısı değerlendirilirken geçersiz işaretçi.

## <a name="1080"></a>1.0.8.0

26 Eylül 2012 yayımlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Sabit bizim betik açan projeyi yolunu elde emin olan yoldur hem Visual Studio hem de komut dosyaları açamaz.

- Sabit bir hata ile kesme noktaları hata ayıklama oturumu, çalışırken oluşturulan Visual Studio'nun kilitlenmesine neden olabilir.

- Visual Studio 2010'da UnityVS nasıl kayıtlı düzeltildi.

## <a name="1070"></a>1.0.7.0

14 Eylül 2012 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Visual Studio 2012 desteği.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Unity'nın davranışı eşleştirmek için düzenleyici ve eklentileri proje dosyalarının oluşturulmasını sabit.

- Çeviri .pdb simgeleri Unity 4'te düzeltilmiştir.

> [!IMPORTANT]
> Visual Studio 2012 desteği nedeniyle birkaç dosyalarını yeniden adlandırın ve başka gezinme vardı. Unity içeri aktarmak için UnityVS paket artık UnityVS 2010 veya UnityVS 2012'de, sırasıyla Visual Studio 2010 ve Visual Studio 2012 için olarak adlandırılır. Bu sürüm ayrıca UnityVS proje dosyalarını yeniden oluşturulduğunu gerektirir.

## <a name="1060---internal-build"></a>1.0.6.0 - iç yapı
12 Eylül 2012 yayımlanan

## <a name="1050"></a>1.0.5.0

10 Eylül 2012 yayımlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Sabit betikleri ve gölgelendiricileri geçersiz xml karakter değilse, proje dosyalarının oluşturulmasını.

- Unity varlık sunucuya bağlanıldığında Unity örnekleri sabit algılanması. Bu, Unity ve Visual Studio hata ayıklayıcı otomatik bağlantısı dosyaları açmak için hataları tetiklenir.

## <a name="1040"></a>1.0.4.0

5 Eylül 2012 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Unity hata ayıklama sembolleri otomatik dönüştürme.

    Bir .NET .dll derlemesi ile kendi ilgili .pdb varlık klasörünüzde varsa, yalnızca derlemenin yeniden içeri aktarın ve UnityVS, Unity'nın komut dosyası altyapısı anlar ve sizin için adım, .NET derlemeleri halinde mümkün olacaktır bir hata ayıklama sembolleri dosyasına .pdb dönüştürür UnityVS.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Yöntemleri veya özellikleri içinde Unity tarafından oluşturulan özel durumları nedeniyle hata ayıklama sırasında UnityVS kilitlenme sorunu düzeltildi.

## <a name="1030"></a>1.0.3.0

4 Eylül 2012 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Unity'de dosyaları açmak için UnityVS kullanımını devre dışı bırakmak için yeni yapılandırma seçeneği.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Sabit UnityEditor başvuruları nesil olmayan Düzenleyicisi projeler için.

- Sabit olmayan Düzenleyicisi projeleri UNITY_EDITOR sembolünün tanımı.

- Çökme, özel durum çubuğu tarafından neden rastgele VS sabit.

## <a name="1020"></a>1.0.2.0

Yayımlanan 30 Ağustos 2012

### <a name="bug-fixes"></a>Hata düzeltmeleri

- PythonTools hata ayıklayıcı sabit çakışıyor.

- Mono.Cecil sabit başvurular.

- Hata düzeltildi nasıl betik derlemelerde alınan Unity'de Unity 4 b7 ile.

## <a name="1010"></a>1.0.1.0

28 Ağustos 2012 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

- Unity 4.0 Beta önizlemesi desteği.

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Özel durumları atma özelliklerini inceleme düzeltildi.

- Temel nesnelere nesneleri incelerken azalan düzeltildi.

- Ekleme noktasını MonoBehavior Sihirbazı için sabit boş açılan listesi.

- Dll içindeki varlık klasörünü sabit tamamlanmasını UnityScript ve hata.

## <a name="1000---initial-release"></a>1.0.0.0 - ilk yayın
22 Ağustos 2012 yayımlanan
