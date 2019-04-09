---
title: Değişiklik günlüğü (Unity, Mac için Visual Studio Araçları) | Microsoft Docs
ms.custom: ''
ms.date: 04/02/2019
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 33a6ac54-d997-4308-b5a0-af7387460849
author: therealjohn
ms.author: johmil
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: 25269189489dab4a51b7f3b45f0aa670e39f50fb
ms.sourcegitcommit: 36f5ffd6ae3215fe31837f4366158bf0d871f7a9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59232633"
---
# <a name="change-log-visual-studio-tools-for-unity-mac"></a>Değişiklik Günlüğü (Unity için Visual Studio Araçları, Mac)
Değişiklik günlüğü Unity için Visual Studio Araçları.

## <a name="2020"></a>2.0.2.0
 2 Nisan 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Unity'nın varlık veritabanı'üzerinde otomatik olarak yenilemek için destek eklendi kaydedin. Bu, varsayılan olarak etkindir ve öyle Unity tarafında, Visual Studio'da bir kod kaydedilirken tetikler. Üzerinde Unity\Refresh Unity'nın AssetDatabase kaydetmek için bu özelliği Tools\Options\Tools devre dışı bırakabilirsiniz.

    -   Çevrimdışı belgeleri için tercih edilen unity yükleme ayarlama desteği eklendi.

    -   Yeni bir düzenleyici ek bağlam menüsü.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Hata Ayıklayıcı:**

    -   Derleme filtreleme ve çerçeve İnceleme boş çerçeveleri ile düzeltildi.

## <a name="2011"></a>2.0.1.1
 26 Mart 2019 yayımlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Geçici olarak olun Mono varsayılan ve yalnızca kullanılabilir hata ayıklayıcı bu belirli sürümü için.

## <a name="2006"></a>2.0.0.6
 26 Mart 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   "Eklemek için Unity ve Yürüt" için destek eklendi.

## <a name="2005"></a>2.0.0.5
 20 Mart 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Proje oluşturma:**

    -   Dış özellikler, çözüm dosyasını işlerken korur.

## <a name="2004"></a>2.0.0.4
 5 Mart 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   API ScriptableObject güncelleştirildi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Şablonlardan kaldırılan ad alanları.

## <a name="2003"></a>2.0.0.3
 5 Mart 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Proje oluşturma:**

    -   Genel ve seri hale getirilmiş alanları artık uyarılar neden olur. Biz otomatik oluşturulan bu iletiler Unity projeleri CS0649 ve IDE0051 Derleyici uyarılarını bastırılmış.

-   **Tümleştirme:**

    -   Daha fazla bir Unity işlem çalışıyorsa belirli bir örneğine eklemek isteyebilir.

-   **Değerlendirme:**

    -   Yerel işlevler için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Hata Ayıklayıcı:**

    -   Özel öznitelik adlandırılmış bağımsız değişkenler üzerinde eski protokol sürümleri kullanılırken okuma düzeltildi.

## <a name="2002"></a>2.0.0.2
 4 Şubat 2019 yayımlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   MonoBehaviour API güncelleştirildi.
   
### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Hata Ayıklayıcı:**

    -   Hata ayıklayıcıda basit değerler ayarlama düzeltildi.

## <a name="2001"></a>2.0.0.1
 Yayın Tarihi: 4 Aralık 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Yükleme paketini kendi kendine kapsama düzeltildi.

## <a name="2000"></a>2.0.0.0
 Yayın Tarihi: 4 Aralık 2018

### <a name="new-features"></a>Yeni Özellikler

-   **Hata Ayıklayıcı:**

    -   Unity hata ayıklayıcı Mac üzerinde aynı çekirdek Unity Hata Ayıklayıcı'dan Windows değiştirilecektir.

    -   Roslyn ile değiştiriliyor NRefactory ifade değerlendirmesi için değiştirildi.

    -   İşaretçiler için destek eklemiştir: başvuru, atama ve işaretçi aritmetiğini (Unity 2018.2 + hem yeni çalışma zamanının bunun için gerekli).

    -   Dizi işaretçisi görünümünü (c++ benzer) için destek eklendi. Bir işaretçi ifadesi olması, ardından virgül ve görmek istediğiniz öğe sayısı.

    -   Zaman uyumsuz yapıları için destek eklendi.

    -   Sözde değişkenler (özel durum ve nesne tanımlayıcılar) için destek eklendi.
    
### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Hata Ayıklayıcı:**

    -   Hatalı biçimlendirilmiş ya da desteklenmeyen ifadeler ile sabit ifade değerlendirmesi.

## <a name="1700"></a>1.7.0.0
 13 Kasım 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Hata Ayıklayıcı:**

    -   Daha fazla istemci bilgileri (IP, makine adı) işleme İliştir iletişim kutusunda eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Hata Ayıklayıcı:**

    -   Visual Studio veya Unity, özellikle 'Unity İşleme İliştir' ulaşmaktan olduğunda dondurma yapma veya oyunu yeniden Unity'nın hata ayıklayıcısı altyapısı ile iletişim kurmak için kullanılan Kitaplığı'nda bir kilitlenme düzeltildi.

-   **Tümleştirme:**

    -   Başka bir varsayılan düzenleyici seçildiğinde sabit Unity eklentisini etkinleştirme.

    -   Sabit Unity dosya şablonu oluşturma.

## <a name="1602"></a>1.6.0.2
 24 Temmuz 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Unity tarafından sabit bir Unity performans hatanın geçici çözümü geri alındı.

## <a name="1601"></a>1.6.0.1
 Yayın Tarihi: 10 Temmuz 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Sabit gölgelendirici kod coloration destekler.

## <a name="1600"></a>1.6.0.0
 26 Haziran 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Sihirbazlar:**

    -   Sabit yazım yanlışı OnApplicationFocus iletisi.

-   **Proje oluşturma:**

    -   Unity performans hatanın geçici çözüm: projeleri oluştururken MonoIslands önbellek.

    -   Taşınabilir pdb mdb için artık yeni Unity çalışma zamanı kullanırken dönüştürmez.

## <a name="1502"></a>1.5.0.2
 18 Nisan 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Temel gölgelendirici kod tamamlama desteği eklendi.

    -   Gölgelendirici dosyaları açıklamalarda geçiş için destek eklendi.

## <a name="1501"></a>1.5.0.1
 28 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Unity proje Gezgininde ek şablonlar için destek eklendi.

## <a name="1500"></a>1.5.0.0
 21 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Algılama ve USB üzerinden bağlı Android oynatıcılarda ekleme desteği eklendi.

## <a name="1403"></a>1.4.0.3
 5 Mart 2018'de yayınlanan

### <a name="new-features"></a>Yeni Özellikler

-   **Proje oluşturma:**

    -   Yeni Proje Oluşturma Aracı'nda Unity 2018.1 desteği eklendi.

-   **Tümleştirme:**

    -   Özel ayarlar için eklenen seçeneği bölmesi.

## <a name="1402"></a>1.4.0.2
 Yayın Tarihi: 24 Ocak 2018

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Proje oluşturma:**

    -   Mono sürüm algılama düzeltildi.

-   **Tümleştirme:**

    -   2018.1 ile zamanlama sorunları düzeltildi ve eklentisini etkinleştirme.

    -   Yeni bir oynatıcı tespit edilirken sabit bildirimleri.

## <a name="1401"></a>1.4.0.1
 23 Ocak 2018'de yayınlanan

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Sabit Genişlet/Daralt klasörlerde çift tıklayın

## <a name="1400"></a>1.4.0.0
 Yayın Tarihi: 13 Aralık 2017

### <a name="new-features"></a>Yeni Özellikler

-   **Proje oluşturma:**

    -   .NET Standard için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Mdb hata ayıklama sembol dönüştürme sabit otomatik pdb.

## <a name="1301"></a>1.3.0.1
 Yayın Tarihi: 12 Aralık 2017

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Dizi boyutu değiştirilmeye çalışılırken Inspector'ı etkileyen EditorPrefs.GetBool sabit dolaylı çağrı.

-   **Sihirbazlar:**

    -   Roslyn bağlam yöntemi eklemeden önce yenileyin.

## <a name="1300"></a>1.3.0.0
 Yayın Tarihi: 20 Kasım 2017

### <a name="new-features"></a>Yeni Özellikler

-   **Sihirbazlar:**

    -   "Uygulama Unity ileti" Sihirbazı eklendi.

    -   Yeni API vs'de için tamamlama Mac 7.4 desteği eklendi.

## <a name="1200"></a>1.2.0.0
 Yayın Tarihi: 23 Ekim 2017

### <a name="new-features"></a>Yeni Özellikler

-   **Hata Ayıklayıcı:**

    -   Taşınabilir hata ayıklama sembol dosyaları için destek eklendi.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Proje oluşturma:**

    -   Ek .dll uzantısı yanlış derleme dosya adına eklenmiş düzeltildi.

    -   Varsayılan 'true' olduğunda AllowAttachedDebuggingOfEditor Unity bayrağı zorlamaz.

## <a name="1103"></a>1.1.0.3
 Yayın Tarihi: 23 Ekim 2017

### <a name="new-features"></a>Yeni Özellikler

-   **Proje oluşturma:**

    -   .NET 4.6 profili için destek eklendi.

## <a name="1102"></a>1.1.0.2
 Yayın Tarihi: 8 Ağustos 2017

### <a name="new-features"></a>Yeni Özellikler

-   **Hata Ayıklayıcı:**

    -   İşleme İliştir'iletişim kutusunda emin değil, başlangıç iliştirmek için hangi Unity.

-   **Proje oluşturma:**

    -   Unity 5.6 kullanıldığında her zaman güvensiz derleme anahtar etkinleştirin.

## <a name="1101"></a>1.1.0.1
 20 Temmuz 2017 tarihinde yayımlandı

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Yerelleştirilmiş kaynaklar için destek eklendi.

## <a name="1100"></a>1.1.0.0
 12 Temmuz 2017 tarihinde yayımlandı

### <a name="new-features"></a>Yeni Özellikler

-   **Tümleştirme:**

    -   Oyuncuların ve düzenleyicileri aracılığıyla ekleme işlemini penceresine ekleme desteği eklendi.

-   **Proje oluşturma:**

    -   Derleme adı başvuruları mcs.rsp dosyalarıyla düzeltildi.

    -   Assembly.json derleme birimler için destek eklendi.

    -   Sabit ile API düzeyleri tanımlar.

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Derleme sırasında sabit gölgelendirici hata iletisi.

## <a name="1001"></a>1.0.0.1
 4 Mayıs 2017 tarihinde yayımlandı

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   **Tümleştirme:**

    -   Etkin belge izleme karma ve normal projeleri ile düzeltildi.

## <a name="1000"></a>1.0.0.0
 3 Mayıs 2017 tarihinde yayımlandı
