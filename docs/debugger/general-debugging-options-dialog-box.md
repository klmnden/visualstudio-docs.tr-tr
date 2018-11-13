---
title: Genel, hata ayıklama, Seçenekler iletişim kutusu | Microsoft Docs
ms.custom: ''
ms.date: 11/09/2018
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.options.General
- VS.ToolsOptionsPages.Debugger.General
- VS.ToolsOptionsPages.Debugger.ENC
- vs.debug.options.ENC
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Options dialog box, debugging
ms.assetid: b33aee0b-43c3-4c26-8ed4-bc673f491503
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e6f53248f1434bd2b089e710daea3420d6d0fdb5
ms.sourcegitcommit: a34b7d4fdb3872865fcf98ba24a0fced58532adc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/12/2018
ms.locfileid: "51561666"
---
# <a name="general-debugging-options"></a>Genel hata ayıklama seçenekleri
Visual Studio hata ayıklayıcısı seçenekleri ayarlamak için seçin **Araçları** > **seçenekleri**, altında **hata ayıklama** seçin veya yanındaki kutuları seçimini  **Genel** seçenekleri. Tüm varsayılan ayarlarını geri yükleyebilirsiniz **Araçları** > **içeri ve dışarı aktarma ayarları** > **tüm ayarları Sıfırla**. Ayarların bir alt kümesini sıfırlamak için ayarlarınızla Kaydet **içeri ve dışarı aktarma ayarları Sihirbazı** test etmek istediğiniz değişiklik yapmadan önce sonra kaydedilmiş ayarlarınızı daha sonra içeri aktarın.
  
Aşağıdakileri ayarlayabilirsiniz **genel** seçenekleri:

**Tüm kesme noktalarını silmeden önce sor**: tamamlamadan önce onay gerektirir **tüm kesme noktalarını Sil** komutu.  
  
**Bir işlem kesildiğinde tüm işlemleri Kes**: tüm işlemler için hata ayıklayıcının bağlı, bir kesme oluştuğunda aynı anda keser.  
  
**Özel durumlar, AppDomain veya yönetilen/yerel sınırları geçtiğinde Kes**: yönetilen veya karma mod hata ayıklama ortak dil çalışma zamanı uygulama etki alanı sınırları veya yönetilen/yerel sınırları çapraz özel durumları yakalayabilir, aşağıdaki koşullar geçerli olur:  
  
1. Yerel kod yönetilen kodu COM birlikte çalışması ve yönetilen kod kullanarak çağırdığında, özel durum oluşturur. Bkz: [COM birlikte çalışma'ya giriş](/dotnet/articles/visual-basic/programming-guide/com-interop/introduction-to-com-interop).  
  
2. 1 uygulama etki alanında çalışan yönetilen koda yönetilen kod 2 uygulama etki alanında çağırır. ve 2 uygulama etki alanındaki kod bir özel durum oluşturur. Bkz: [uygulama etki alanlarıyla programlama](/dotnet/articles/framework/app-domains/index).  

3. Kod, yansıma kullanarak bir işlev çağırır ve bu işlev bir özel durum oluşturur. Bkz: [yansıma](/dotnet/framework/reflection-and-codedom/reflection).  
  
Koşullarda 2 ve 3, özel durum bazen yönetilen kod tarafından yakalandı `mscorlib` yerine ortak dil çalışma zamanı. Bu seçenek etkilemez tarafından yakalanan özel bozucu `mscorlib`.  
  
**Adres seviyesinde hata ayıklamayı**: Gelişmiş adres düzeyinde hata ayıklama özellikleri etkinleştirir ( **ayrıştırılmış kodu** penceresinde **kaydeder** penceresi ve adres kesme noktaları).  
  
- **Kaynak kullanılamıyorsa ayrıştırılmış Kodu Göster**: otomatik olarak gösterir **ayrıştırılmış kodu** kaynak olduğu kullanılabilir kod hata ayıklaması yaparken penceresi.  
  
**Kesme noktası filtrelerini etkinleştir**: yalnızca belirli işlemleri, iş parçacıklarını veya bilgisayarları etkiler, kesme noktalarında filtreler ayarlamanızı sağlar.  
 
**Yeni özel durum Yardımcısını Kullan**: özel durum Yardımcısını değiştirir. özel durum Yardımcısı (Visual Studio 2017) sağlar.
  
> [!NOTE]
> Yönetilen kod için bu seçenek daha önceden çağrıldığından **özel durum Yardımcısını** . 
  
**Sadece benim kodumu etkinleştir**: hata ayıklayıcı görüntüler ve adımları kullanıcı kodu ("kodum") yalnızca, sistem kodunu ve en iyisi olan veya olmayan hata ayıklama simgeleri diğer kod yoksayılıyor.

- **(Sadece yönetilen) hiç kullanıcı kodu yoksa uyar**: yalnızca kendi kodum ile hata ayıklama başladığında, bu seçenek, kullanıcı kodu ("kodum") olup olmadığını sizi uyarır. 

**Etkinleştirme .NET Framework kaynak Adımlamayı**: hata ayıklayıcı, .NET Framework kaynağına ilerlemesine olanak sağlar. Bu seçeneği etkinleştirmek otomatik olarak Just My Code'u devre dışı bırakır. .NET framework sembolleri bir önbellek konumuna karşıdan yüklenir. İle önbellek konumunu değiştirmek **seçenekleri** iletişim kutusu, **hata ayıklama** kategori **sembolleri** sayfası.  
  
**Özellikler ve işleçler (sadece yönetilen) üzerinden adımla**: hata ayıklayıcı, yönetilen kod içindeki özellikler ve işleçlerin içine adımlamasını engeller.  
  
**Özellik değerlendirmesini ve diğer örtük işlev çağrılarını ekinleştir**: özelliklerin ve örtülü işlev otomatik olarak değerlendirilmesini etkinleştirir değişkenler pencerelerinde çağırır ve **QuickWatch** iletişim kutusu.  
  
- **Değişken pencerelerindeki nesnelerde dize dönüştürme işlevini çağırma (C# ve yalnızca JavaScript)**: değişken pencerelerinde nesneleri değerlendirirken bir örtük dize dönüştürmesi çağrısı yürütür. Sonuç tür adı yerine bir dize olarak görüntülenir. Yalnızca C# kodunda hata ayıklama sırasında uygulanır. Bu ayar DebuggerDisplay özniteliği tarafından geçersiz kılınmış olabilir (bakın [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md)).  
  
**Kaynak sunucusu desteğini etkinleştir**: Visual Studio hata ayıklayıcıya SrcSrv uygulayan kaynak sunuculardan kaynak dosyaları almak için (`srcsrv.dll`) protokolü. Team Foundation Server ve Windows için hata ayıklama araçları protokol uygulayan iki kaynak sunucular olan. SrcSrv kurulumu hakkında daha fazla bilgi için bkz. [SrcSrv](/windows-hardware/drivers/debugger/srcsrv) belgeleri. Ayrıca bkz [belirtin, sembol (.pdb) ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).  
  
> [!IMPORTANT]
> Çünkü okuma *.pdb* dosyaları, dosyalarda rasgele kod yürütebilir, sunucunun güvenilir olduğundan emin olun.  
  
- **Kaynak sunucusu tanılama iletilerini çıkış penceresine Yazdır**: kaynak sunucu desteği etkinleştirildiğinde, bu ayar tanılama görüntüsünü etkinleştirir.  
  
- **Kısmi güven derlemeleri (sadece yönetilen) için kaynak sunucuya izin**: Bu ayar, kaynak sunucu desteği etkinleştirildiğinde, kısmi güven derlemeleri için kaynakları almayarak varsayılan davranışını geçersiz kılar.  

- **Sormadan güvenilmeyen kaynak sunucu komutlarını her zaman Çalıştır**: Bu ayar, kaynak sunucu desteği etkinleştirildiğinde, güvenilmeyen bir komutu çalıştırırken sormadan varsayılan davranışını geçersiz kılar.

**Kaynak bağlantısı desteğini etkinleştir**: kaynak dosyalarını indirmek için Visual Studio hata ayıklayıcıya bildirir *.pdb* kaynak bağlantısı bilgiler içeren dosyaları. Kaynak bağlantısı hakkında daha fazla bilgi için bkz: [kaynak bağlantı belirtimi](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/source_link.md).

> [!IMPORTANT]
>  Kaynak bağlantısı http veya https kullanarak dosyaları indirileceğinden güvendiğinizden emin olun *.pdb* dosya.  
  
- **Geri Git kimlik bilgisi Yöneticisi kimlik doğrulaması için Fall için tüm kaynak bağlantısı isteklerine**: etkin olduğunda kaynak bağlantı desteği ve kaynak bağlantısı isteği başarısız kimlik doğrulaması, Visual Studio sonra Git Credential Manager'ı çağırır.

**Kesme noktaları ve geçerli deyim (yalnızca C++) için satırın tamamını vurgulayın**: hata ayıklayıcı bir kesme noktası veya geçerli ifadeyi Vurguladığında tüm satırı vurgular.  
  
**Özgün sürümle kaynak dosyaların uyuşmasını gerektir**: kaynak dosyası hata ayıklamasını yaptığınız çalıştırılabilir dosyayı oluşturmak için kullanılan kaynak kodu sürümüyle eşleşen doğrulamak için hata ayıklayıcıya bildirir. Sürüm eşleşmiyor, eşleşen bir kaynak bulmanız istenir. Eşleşen bir kaynak bulunamıyorsa, kaynak kodu hata ayıklama sırasında görüntülenmez. 
  
**Tüm çıkış penceresi metnini yürütme penceresine yeniden yönlendir**: hata ayıklayıcı tüm normalde içinde görünecek iletileri gönderir **çıkış** penceresine **hemen** penceresi yerine.  
  
**Nesnelerin ham yapısını değişkenler pencerelerinde Göster**: tüm nesne yapısı görünümü özelleştirmelerini devre dışı bırakır. Görünüm özelleştirmeleri hakkında daha fazla bilgi için bkz. [.managed nesnelerin özel görünümlerini oluşturma](../debugger/create-custom-views-of-dot-managed-objects.md).  
  
**Modül yükleme (sadece yönetilen) JIT iyileştirmesini bastır**: hata ayıklayıcı JIT derlenmiş ve bir modül yüklendiğinde yönetilen kodun JIT iyileştirmesini devre dışı bırakır. İyileştirme devre dışı bırakma bazı sorunların hatalarını ayıklamak performans rağmen çoğaltamaz kolaylaştırabilir. Yalnızca kendi Kodum'u kullanıyorsanız, JIT gizleme kullanıcı kodu ("kodum") görüntülenecek kullanıcı olmayan kod iyileştirme neden olabilir. Daha fazla bilgi için [JIT iyileştirmesi ve hata ayıklaması](../debugger/jit-optimization-and-debugging.md).

**JavaScript (Chrome, Edge ve IE) ASP.NET için hata ayıklamayı**: ASP.NET uygulamaları için betik hata ayıklayıcısı sağlar. Chrome'da ilk kez kullanıldığında, yüklemiş olduğunuz Chrome uzantıları etkinleştirmek için tarayıcıda oturum gerekebilir. Eski davranışa dönmek için bu seçeneği devre dışı bırakın.    

**UWP JavaScript uygulamaları (Deneysel) için Edge geliştirici araçlarını etkinleştir**: edge'de UWP JavaScript uygulamaları için geliştirici araçları sağlar.

**ASP.NET için eski Chrome JavaScript hata ayıklayıcısını etkinleştir**: ASP.NET uygulamaları için eski Chrome JavaScript komut dosyası hata ayıklayıcı sağlar. Chrome'da ilk kez kullanıldığında, yüklemiş olduğunuz Chrome uzantıları etkinleştirmek için tarayıcıda oturum gerekebilir.

**Visual Studio'yu yönetici olarak çalışırken Chrome JavaScript hata ayıklama başlatmak için Deneysel gibi kullanabileceğiniz**: Chrome JavaScript hata ayıklama sırasında başlatmak için yeni bir yolunu denemek için Visual Studio'yu söyler.

**Dll dışarı aktarmaları (yalnızca yerel) yük**: dll dışarı aktarma tablolarını yükler. Dll dışa aktarma tablolarının sembol bilgilerini Windows iletileri, Windows yordamları (WindowProcs), COM nesneleri veya sıralama veya sembolleri olmayan herhangi bir dll ile çalışıyorsanız yararlı olabilir. Dışa aktarma bilgilerini okuma dll bazı ek okumalar içerir. Bu nedenle, bu özellik varsayılan olarak kapalıdır.  
  
Bir DLL'nin dışa aktarma tablosunda hangi sembollerin kullanılabilir görmek için `dumpbin /exports`. Semboller tüm 32-bit sistem dll için kullanılabilir. Okuyarak `dumpbin /exports` çıkışı, alfasayısal olmayan karakterler de dahil tam işlev adını görebilirsiniz. Bu, bir işlev bir kesme noktası ayarlamak için yararlıdır. Dll dışarı aktarma tablolarındaki işlev adları hata ayıklayıcıda başka bir yerde kesilmiş görünebilir. Aramalar geçerli işlev en üstte (en yoğun şekilde iç içe geçmiş) olacak şekilde arama sırasıyla listelenir. Daha fazla bilgi için [dumpbin/EXPORTS](/cpp/build/reference/dash-exports).  
  
**Show Paralel Yığınlar diyagramını aşağıdan yukarıya**: hangi görüntülenme yönünü denetler **Paralel Yığınlar** penceresi.
  
**Yazılan veriler değeri değiştirmiyorsa GPU bellek erişimi özel durumlarını Yoksay**: veri değişmediyse hata ayıklama sırasında algılanan yarış durumlarını yoksayar. Daha fazla bilgi için [GPU kodunda hata ayıklama](../debugger/debugging-gpu-code.md).  
  
**Yönetilen Uyumluluk modunu kullan**: varsayılan hata ayıklama altyapısı bu senaryoları sağlamak için eski bir sürüm ile değiştirir:  
  
- Dışında bir .NET Framework dili kullanıyorsunuz C#, VB veya F# kendi ifade değerlendiricisi sağlayan (buna C + dahildir +/ CLI).  
  
- Karışık modda hata ayıklama sırasında C++ projeleri için Düzenle ve Devam Et'i etkinleştirmek istediğiniz.  
  
> [!NOTE]
> Yönetilen uyumluluk modu yalnızca hata ayıklama altyapısı varsayılan uygulanan bazı özellikler devre dışı bırakır. 

**Eski kullanın C# ve VB ifade değerlendiricilerini**: hata ayıklayıcı, Visual Studio 2013'ün kullanacak C#Visual Studio 2015 Roslyn tabanlı ifade değerlendiricilerini yerine /VB ifade değerlendiricilerini.    
  
**(Sadece yönetilen) güvenli olmayan işlemlere karşı özel hata ayıklama görselleştiricileri kullanıldığında uyar**: Visual Studio sizi uyarır kod hataları ayıklanmış işlemde çalışan bir özel hata ayıklama görselleştiricisi kullanırken çalıştırdığınızdan güvenli olmayan kod.  
  
**Windows hata ayıklama yığın ayırıcısını (yalnızca yerel) etkinleştirme**: yığın tanılamayı geliştirme amacıyla windows hata ayıklama yığınındaki sağlar. Bu seçenek etkinleştirildiğinde, hata ayıklama performansını etkiler.  
  
**XAML için UI hata ayıklama araçlarını etkinleştir**: Live Visual Tree ve Live özellik keşfedin windows hata ayıklamaya başladığınızda görünür (**F5**) desteklenen proje türü. Daha fazla bilgi için [hata ayıklama sırasında XAML İnceleme özellikleri](../debugger/inspect-xaml-properties-while-debugging.md).  
  
- **Seçilen öğeleri Canlı görsel ağaç Önizleme**: XAML öğesi bağlamı seçiliyse seçili ayrıca **Live Visual Tree** penceresi.  
  
- **Çalışma zamanı araçlarını uygulamada Göster**: gösterir **Live Visual Tree** ayıklanmakta olan XAML uygulamanın ana pencere bir araç komutları. Bu seçenek, Visual Studio 2015 güncelleştirme 2'de sunulmuştur. 

- **XAML Düzenle ve Devam Et'i etkinleştir**: Düzen ve XAML kodu özelliğiyle devam olanak tanır. 
  
**Hata ayıklama sırasında tanılama araçları etkinleştirme**: **tanılama araçları** ayıklarken penceresi görüntülenir.
  
**Hata ayıklama sırasında PerfTip geçen süresini göster**: hata ayıklaması yapıyorsanız Kod penceresi belirtilen yöntem çağrısının geçen süreyi görüntüler.  
  
**Düzenle ve Devam Et'i etkinleştir**: hata ayıklarken Düzenle ve Devam Et işlevini destekler.  
  
- **Yerel Düzenle ve Devam Et'i etkinleştir**: Düzen ve yerel C++ kodunu ayıklarken İşlevselliği devam edebilirsiniz. Daha fazla bilgi için [Düzenle ve devam et (Visual C++)](../debugger/edit-and-continue-visual-cpp.md).  
  
- **Değişiklikleri Uygula (yalnızca yerel) üzerinde devam**: Visual Studio otomatik olarak derler ve bir kesme durumundan işlemine devam etmek, yapmış olduğunuz bekleyen kod değişiklikleri uygular. Seçilmezse, kullanarak değişiklikleri uygulamak seçebileceğiniz **kod değişikliklerini uygulama** altında madde **hata ayıklama** menüsü.  
  
- **(Yalnızca yerel) eski kod hakkında uyar**: eski kod hakkında uyarı alın.    

**Çalıştır'ı tıklatın Göster düğmesini düzenleyicide hata ayıklama sırasında**: Bu seçenek belirlendiğinde, [tıklanan satıra kadar Çalıştır](debugger-feature-tour.md#run-to-a-point-in-your-code-quickly-using-the-mouse) hata ayıklama sırasında düğmesi gösterilir.

**Hata ayıklama durdurulduğunda Konsolu otomatik olarak kapatmak**: hata ayıklama oturumu sonunda Konsolu kapatmak için Visual Studio söyler.
  
## <a name="options-available-in-older-versions-of-visual-studio"></a>Visual Studio'nun eski sürümlerinde kullanılabilir seçenekleri

Visual Studio'nun daha eski bir sürümü kullanıyorsanız, bazı ek seçenekler mevcut olabilir.

**Özel durum Yardımcısını**: yönetilen kod için özel durum Yardımcısı'nı etkinleştirir. Visual Studio 2017'de, özel durum Yardımcısını özel durum Yardımcısı değiştirildi.

**Çağrı yığınını işlenmeyen özel durumlar üzerinde bırakma**: neden **çağrı yığını** çağrı yığınını işlenmeyen özel durum oluşmadan önceki noktaya geri almak için penceresi. 

**(Yalnızca yerel) sembol yoksa uyar**: hata ayıklayıcı sembol bilgisi olan bir programı hata ayıklaması yaparken, bir uyarı iletişim kutusu görüntüler. 

**Hata ayıklamayı başlatma sırasında devre dışı bırakılıp bırakılmadığını uyar**: hata ayıklayıcı komut dosyası ile hata ayıklaması devre dışı olarak başlatıldığında bir uyarı iletişim kutusu görüntüler.

**Yerel Uyumluluk modunu kullan**: Bu seçenek belirlendiğinde, hata ayıklayıcı yeni yerel hata ayıklayıcı yerine Visual Studio 2010 yerel hata ayıklayıcı kullanır.  
  
- .NET C++ kodunu ayıklarken yeni hata ayıklama motoru değerlendirilirken .NET C++ deyimleri desteklemediğinden bu seçeneği kullanın. Ancak, çalışması için geçerli hata ayıklayıcı mantığınız bağımlı birçok özelliği yerel uyumluluk modu etkinleştirme devre dışı bırakır. Örneğin, yerleşik türler ister için eski motoru birçok görselleştiriciler eksik `std::string` Visual Studio 2015 projelerinde.   Visual Studio 2013 proje, bu gibi durumlarda en iyi hata ayıklama deneyimi için kullanır.

## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio’da hata ayıklama](../debugger/index.md)  
 [Hata ayıklayıcısı özellik turu](../debugger/debugger-feature-tour.md)
