---
title: Genel, hata ayıklama, Seçenekler Iletişim kutusu | Microsoft Docs
ms.date: 11/09/2018
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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 03634b5a2bd1417e75f843fd9026712313f1923d
ms.sourcegitcommit: 0e482cfc15f809b564c3de61646f29ecd7bfcba6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/14/2019
ms.locfileid: "70987638"
---
# <a name="general-debugging-options"></a>Genel hata ayıklama seçenekleri

Visual Studio hata ayıklayıcısı seçeneklerini ayarlamak için **Araçlar** > **Seçenekler**' i seçin ve **hata ayıklama** altında **genel** Seçenekler ' in yanındaki kutuları seçin veya seçimi kaldırın. Tüm varsayılan ayarları **Araçlar** > **içeri aktarma ve dışarı aktarma ayarları** > **tüm ayarları Sıfırla**geri yükleyebilirsiniz. Bir ayar alt kümesini sıfırlamak için, test etmek istediğiniz değişiklikleri yapmadan önce ayarlarınızı **içeri ve dışarı aktarma Sihirbazı** ile kaydedin, sonra kaydedilen ayarlarınızı daha sonra içeri aktarın.

Aşağıdaki **genel** seçenekleri belirleyebilirsiniz:

**Tüm kesme noktalarını silmeden önce sor**: **Tüm kesme noktalarını Sil** komutu tamamlanmadan önce onay gerektirir.

**Bir işlem kesildiğinde tüm Işlemleri kes**: Bir kesme oluştuğunda, hata ayıklayıcının eklendiği tüm süreçler eşzamanlı olarak kesilir.

**Özel durum AppDomain veya yönetilen/yerel sınırlar olduğunda kes**: Yönetilen veya karma mod hata ayıklamada, ortak dil çalışma zamanı, aşağıdaki koşullar doğru olduğunda, uygulama etki alanı sınırları veya yönetilen/yerel sınırları karşılıklı yapan özel durumları yakalayabilir:

1. Yerel kod, yönetilen kodu COM birlikte çalışabilirliği kullanarak çağırdığında ve yönetilen kod bir özel durum oluşturduğunda. Bkz. [com birlikte çalışabilirliğine giriş](/dotnet/articles/visual-basic/programming-guide/com-interop/introduction-to-com-interop).

2. Uygulama etki alanı 1 ' de çalıştırılan yönetilen kod, uygulama etki alanı 2 ' deki Yönetilen kodu çağırdığında ve uygulama etki alanı 2 ' deki kod bir özel durum oluşturur. Bkz. [uygulama etki alanlarıyla programlama](/dotnet/articles/framework/app-domains/index).

3. Kod, yansıma kullanarak bir işlevi çağırdığında ve bu işlev bir özel durum oluşturursa. Bkz. [yansıma](/dotnet/framework/reflection-and-codedom/reflection).

2 ve 3. koşullarda, özel durum bazen ortak dil çalışma zamanı yerine içindeki `mscorlib` yönetilen kod tarafından yakalanır. Bu seçenek tarafından `mscorlib`yakalanan özel durumların kesilmesini etkilemez.

**Adres düzeyinde hata ayıklamayı etkinleştir**: Adres düzeyinde hata ayıklama için gelişmiş özellikleri ( **ayrıştırılmış** pencere, **Yazmaçları** penceresi ve adres kesme noktaları) sağlar.

- **Kaynak kullanılamıyorsa ayrıştırılmış derlemeyi göster**:   , Kaynağın kullanılamadığı kodda hata ayıklarken **ayrıştırma** penceresini otomatik olarak gösterir.

**Kesme noktası filtrelerini etkinleştir**: Yalnızca belirli işlemlerin, iş parçacıklarının veya bilgisayarların etkilenmeleri için kesme noktalarında filtre ayarlamanıza olanak sağlar.

**Yeni özel durum yardımcısını kullanın**: Özel durum yardımcısını değiştiren özel durum yardımcısını sunar. (Özel durum Yardımcısı, Visual Studio 2017 ' den itibaren desteklenir)

> [!NOTE]
> Yönetilen kod için bu seçenek daha önce **özel durum Yardımcısı 'Nı etkinleştir** olarak adlandırılmıştı.

**Yalnızca kendi kodum etkinleştir**: Hata ayıklayıcı yalnızca Kullanıcı kodu ("My Code") içinde görüntülenir ve sistem kodunu ve en iyileştirilmiş veya hata ayıklama sembolleri olmayan diğer kodu yoksayar.

- **Başlatma üzerinde Kullanıcı kodu yoksa uyar (yalnızca yönetilen)** :   Hata ayıklama Yalnızca kendi kodum etkinken başlatıldığında, Kullanıcı kodu ("My Code") olmadığında bu seçenek sizi uyarır.

**.NET Framework kaynak adımlamayı etkinleştir**: Hata ayıklayıcının .NET Framework kaynak üzerinde adıma çalışmasına izin verir. Bu seçeneğin etkinleştirilmesi Yalnızca kendi kodum otomatik olarak devre dışı bırakır. .NET Framework semboller, bir önbellek konumuna indirilir. Önbellek konumunu **Seçenekler** iletişim kutusu, **hata ayıklama** kategorisi, **semboller** sayfası ile değiştirin.

**Özellikler ve işleçler üzerinde adımla (yalnızca yönetilen)** : Hata ayıklayıcının Yönetilen koddaki Özellikler ve işleçlere erişmesini önler.

**Özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştirin**: Değişkenler Windows ve **QuickWatch** iletişim kutusunda özelliklerin ve örtük işlev çağrılarının otomatik değerlendirmesini etkinleştirir.

- **Değişkenler Windows 'daki (C# ve yalnızca JavaScript) nesnelerde dize dönüştürme işlevini çağırın**: Değişkenler penceresinde nesneleri değerlendirirken örtük bir dize dönüştürme çağrısı yürütür. Sonuç tür adı yerine bir dize olarak görüntülenir. Yalnızca C# kodda hata ayıklanırken geçerlidir. Bu ayar DebuggerDisplay özniteliği tarafından geçersiz kılınabilir (bkz. [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md)).

**Kaynak sunucu desteğini etkinleştir**: Visual Studio hata ayıklayıcısına srcsrv (`srcsrv.dll`) protokolünü uygulayan kaynak sunuculardan kaynak dosyaları almasını söyler. Team Foundation Server ve Windows için hata ayıklama araçları, protokolü uygulayan iki kaynak sunucularıdır. SrcSrv kurulumu hakkında daha fazla bilgi için bkz. [srcsrv](/windows-hardware/drivers/debugger/srcsrv) belgeleri. Ayrıca bkz. [simge (. pdb) ve kaynak dosyaları belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).

> [!IMPORTANT]
> *. Pdb* dosyalarını okuma dosyalarında rastgele kod yürütebildiğinden, sunucuya güvendiğinizden emin olun.

- **Kaynak sunucusu tanılama Iletilerini çıkış penceresine Yazdır**:   Kaynak sunucu desteği etkinleştirildiğinde, bu ayar tanılama görüntüsünü etkinleştirir.

- **Kısmi güven derlemeleri (yalnızca yönetilen) için kaynak sunucuya Izin ver**:   Kaynak sunucu desteği etkinleştirildiğinde, bu ayar kısmi güven derlemeleri için kaynak almamanın varsayılan davranışını geçersiz kılar.

- **Güvenilir olmayan kaynak sunucu komutlarını her zaman sormadan Çalıştır**:   Kaynak sunucu desteği etkinleştirildiğinde, bu ayar Güvenilmeyen bir komutu çalıştırırken sorma işleminin varsayılan davranışını geçersiz kılar.

**Kaynak bağlantısı desteğini etkinleştir**: Visual Studio hata ayıklayıcısına kaynak bağlantı bilgilerini içeren *. pdb* dosyaları için kaynak dosyaları indirmelerini söyler. Kaynak bağlantısı hakkında daha fazla bilgi için bkz. [kaynak bağlantı belirtimi](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/source_link.md).

> [!IMPORTANT]
> Kaynak bağlantısı, http veya https kullanarak dosyaları indirileceği için, *. pdb* dosyasına güvendiğinizden emin olun.

- **Tüm kaynak bağlantısı istekleri Için git Credential Manager kimlik doğrulamasına geri dön**:   Kaynak bağlantısı desteği etkinken ve bir kaynak bağlantı isteği kimlik doğrulaması başarısız olursa, Visual Studio git kimlik bilgileri yöneticisini çağırır.

**Kesme noktaları ve geçerli ifade için tüm satırı VurgulaC++ (yalnızca)** : Hata ayıklayıcı bir kesme noktasını veya geçerli ifadeyi vurgualdığında, tüm satırı vurgular.

**Kaynak dosyalarının özgün sürümle tam olarak eşleşmesini gerektir**: Hata ayıklayıcıya bir kaynak dosyanın, hata ayıklaması yaptığınız yürütülebilir dosyayı oluşturmak için kullanılan kaynak kodun sürümüyle eşleştiğini doğrulamasını söyler. Sürüm eşleşmediği zaman, eşleşen bir kaynak bulmanız istenir. Eşleşen bir kaynak bulunamazsa, hata ayıklama sırasında kaynak kodu gösterilmez.

**Tüm çıkış penceresi metnini komut penceresine yeniden yönlendir**: Genellikle **Çıkış** penceresinde görüntülenen tüm hata ayıklayıcı iletilerini **hemen** bir pencereye gönderir.

**Değişkenler penceresinde nesnelerin ham yapısını göster**: Tüm nesne yapısı görünümü özelleştirmelerini kapatır. Özelleştirmeleri görüntüle hakkında daha fazla bilgi için bkz [. yönetilen nesnelerin özel görünümlerini oluşturma](../debugger/create-custom-views-of-dot-managed-objects.md).

**Modül YÜKLEMESINDE JIT iyileştirmesini bastır (yalnızca yönetilen)** : Modül yüklendiğinde yönetilen kodun JıT iyileştirmesini devre dışı bırakır ve hata ayıklayıcı eklendiğinde JıT derlenir. İyileştirmenin devre dışı bırakılması, performans masrafına karşın bazı sorunların hatalarını ayıklamanızı kolaylaştırabilir. Yalnızca kendi kodum kullanıyorsanız, JıT iyileştirmesini gizleme Kullanıcı dışı kodun kullanıcı kodu ("My Code") olarak görünmesine neden olabilir. Daha fazla bilgi için bkz. [JIT İyileştirmesi ve hata ayıklama](../debugger/jit-optimization-and-debugging.md).

**ASP.net Için JavaScript hata ayıklamasını etkinleştir (Chrome, Edge ve IE)** : ASP.NET uygulamaları için betik hata ayıklayıcısını etkinleştirilir. Chrome 'da ilk kez kullanırken, yüklemiş olduğunuz Chrome uzantılarını etkinleştirmek için tarayıcıda oturum açmanız gerekebilir. Eski davranışa dönmek için bu seçeneği devre dışı bırakın.

**UWP JavaScript uygulamaları (deneysel) Için Edge geliştirici araçları etkinleştirme**: Microsoft Edge 'de UWP JavaScript uygulamaları için geliştirici araçları sunar.

**ASP.NET için eski Chrome JavaScript hata ayıklayıcısını etkinleştir**: ASP.NET uygulamaları için eski Chrome JavaScript betiği hata ayıklayıcısını sunar. Chrome 'da ilk kez kullanırken, yüklemiş olduğunuz Chrome uzantılarını etkinleştirmek için tarayıcıda oturum açmanız gerekebilir.

**Visual Studio 'Yu yönetici olarak çalıştırırken Chrome JavaScript hata ayıklamayı başlatmak için deneysel yol kullanın**: Visual Studio 'Nun, JavaScript hata ayıklaması sırasında Chrome 'ı başlatmak için yeni bir yol denemesini söyler.

**DLL dışarı aktarmaları yükle (yalnızca yerel)** : DLL dışarı aktarma tablolarını yükler. DLL dışarı aktarma tablolarından sembol bilgileri, Windows iletileri, Windows yordamları (WindowProcs), COM nesneleri veya sıralama ya da sembolleri olmayan herhangi bir dll ile çalışıyorsanız yararlı olabilir. Dll dışa aktarma bilgilerini okuma bazı ek yük içerir. Bu nedenle, bu özellik varsayılan olarak kapalıdır.

Dll 'nin dışarı aktarma tablosunda hangi simgelerin kullanılabildiğini görmek için kullanın `dumpbin /exports`. Semboller, 32 bit sistem dll 'si için kullanılabilir. Okuyarak `dumpbin /exports` çıkışı, alfasayısal olmayan karakterler de dahil tam işlev adını görebilirsiniz. Bu, bir işlev bir kesme noktası ayarlamak için yararlıdır. DLL dışarı aktarma tablolarındaki işlev adları, hata ayıklayıcının başka bir yerinde kesilmiş görünebilir. Aramalar geçerli işlev en üstte (en yoğun şekilde iç içe geçmiş) olacak şekilde arama sırasıyla listelenir. Daha fazla bilgi için [dumpbin/EXPORTS](/cpp/build/reference/dash-exports).

**Paralel Yığınlar diyagramını aşağıdan yukarı göster**: Yığınların **Paralel Yığınlar** penceresinde Görüntülenme yönünü denetler.

**Yazılan veriler değeri değiştirmediyse, GPU bellek erişimi özel durumlarını yoksayın**: Veriler değişmediyse hata ayıklama sırasında algılanan yarış durumlarını yoksayar. Daha fazla bilgi için bkz. [GPU kodunda hata ayıklama](../debugger/debugging-gpu-code.md).

**Yönetilen uyumluluk modunu kullan**: Bu senaryoları etkinleştirmek için varsayılan hata ayıklama altyapısını eski bir sürümle değiştirir:

- Kendi Ifade değerlendiricisi (Bu/CLI dahil C# F# C++) sağlayan, Visual Basic veya dışında .NET Framework bir dil kullanıyorsunuz.

- Karışık modda hata ayıklama sırasında projeler için C++ Düzenle ve devam et 'i etkinleştirmek istiyorsunuz.

> [!NOTE]
> Yönetilen Uyumluluk modunu seçme, yalnızca varsayılan hata ayıklama altyapısında uygulanan bazı özellikleri devre dışı bırakır. Eski hata ayıklama altyapısı, Visual Studio 2012 ' de değiştirilmiştir.

**Eski C# ve vb Expression değerlendiricileri kullanın**: Hata ayıklayıcı, Visual Studio 2015 C# Roslyn tabanlı ifade değerlendiricileri yerine Visual Studio 2013 veya Visual Basic Expression değerlendiricileri kullanır.

**Güvenli olmayan işlemlere karşı özel hata ayıklama görselleştiricileri kullanıldığında uyar (yalnızca yönetilen)** : Visual Studio, hata ayıklama işleminde kod çalıştıran özel bir hata ayıklayıcı görselleştiricisi kullanırken, güvenli olmayan kod çalıştırdığından sizi uyarır.

**Windows hata ayıklama yığın ayırıcısını etkinleştir (yalnızca yerel)** : Yığın tanılamayı geliştirmek için Windows hata ayıklama yığını 'nı sağlar. Bu seçeneğin etkinleştirilmesi, hata ayıklama performansını etkiler.

**XAML için Kullanıcı arabirimi hata ayıklama araçlarını etkinleştir**: Canlı görsel ağaç ve canlı özelliği, hata ayıklamayı başlattığınızda (**F5**) desteklenen bir proje türü olarak görüntülenir. Daha fazla bilgi için bkz. [hata ayıklama SıRASıNDA xaml özelliklerini inceleme](../debugger/inspect-xaml-properties-while-debugging.md).

- **Canlı görsel ağaçtaki seçili öğeleri önizleyin**:   Bağlamı seçili olan XAML öğesi, **canlı görsel ağaç** penceresinde de seçilidir.

- **Çalışma zamanı araçlarını uygulamada göster**: Hata ayıklamakta olan XAML uygulamasının ana penceresindeki bir araç çubuğunda **canlı görsel ağaç** komutlarını gösterir. Bu seçenek, Visual Studio 2015 güncelleştirme 2 ' de sunulmuştur.

- **Xaml etkin yeniden yüklemeyi etkinleştir**: Uygulamanız çalışıyorsa XAML kodu ile XAML etkin yeniden yükleme özelliğini kullanmanıza olanak sağlar. (Bu özellik daha önce "XAML Düzenle ve devam et" olarak adlandırılmıştı)

**Hata ayıklarken tanılama araçları etkinleştir**: Hata ayıklarken **Tanılama araçları** pencere görüntülenir.

**Hata ayıklama sırasında Perftıp geçen süreyi göster**: Kod penceresi, hata ayıklarken belirli bir yöntem çağrısının geçen süresini görüntüler.

**Düzenle ve devam et 'ı etkinleştir**: Hata ayıklarken Düzenle ve devam et işlevlerini sağlar.

- **Yerel Düzenle ve devam et 'ı etkinleştir**: Yerel C++ kodda hata ayıklarken Düzenle ve devam et işlevini kullanabilirsiniz. Daha fazla bilgi için [Düzenle ve devam et (Visual C++)](../debugger/edit-and-continue-visual-cpp.md).

- **Değişiklikleri devam ederken Uygula (yalnızca yerel)** : Visual Studio, işleme bir kesme durumundan devam ederken yaptığınız bekleyen kod değişikliklerini otomatik olarak derler ve uygular. Seçili değilse, **hata ayıklama** menüsünün altındaki **kod değişikliklerini Uygula** öğesini kullanarak değişiklikleri uygulamayı seçebilirsiniz.

- **Eski kod hakkında uyar (yalnızca yerel)** :   Eski kod hakkında uyarı alın.

**Hata ayıklama sırasında düzenleyicide tıklama düğmesine tıklayarak göster**: Bu seçenek belirlendiğinde, hata ayıklama sırasında [tıklama düğmesine Çalıştır](../debugger/debugger-feature-tour.md#run-to-a-point-in-your-code-quickly-using-the-mouse) düğmesi gösterilir.

**Hata ayıklama durdurulduğunda konsolu otomatik olarak kapat**: Visual Studio 'Yu hata ayıklama oturumunun sonunda konsolunu kapatmasını söyler.

::: moniker range=">= vs-2019" 
**Hızlı ifade değerlendirmesini etkinleştir (yalnızca yönetilen)** : Hata ayıklayıcının basit özelliklerin ve yöntemlerin yürütülmesini taklit ederek daha hızlı değerlendirmeyi denemesini sağlar.
::: moniker-end

## <a name="options-available-in-older-versions-of-visual-studio"></a>Visual Studio 'nun eski sürümlerinde kullanılabilen seçenekler

Visual Studio 'nun eski bir sürümünü kullanıyorsanız bazı ek seçenekler mevcut olabilir.

**Özel durum yardımcısını etkinleştirin**: Yönetilen kod için özel durum yardımcısını sunar. Visual Studio 2017 ' den başlayarak, özel durum Yardımcısı özel durum yardımcısını değiştirdi.

**İşlenmeyen özel durumlarda çağrı yığınını geriye doğru izleme**: **Çağrı yığını** penceresinin, işlenmeyen özel durum olmadan önce çağrı yığınını noktaya geri almasına neden olur.

**Başlatma üzerinde hiçbir sembol yoksa uyar (yalnızca yerel)** : Hata ayıklayıcının simge bilgilerine sahip olmadığı bir programda hata ayıklaması yaptığınızda bir uyarı iletişim kutusu görüntüler.

**Başlatma sırasında betik hata ayıklaması devre dışıysa uyar**: Hata ayıklayıcı komut dosyası hata ayıklama devre dışıyken başlatıldığında bir uyarı iletişim kutusu görüntüler.

**Yerel uyumluluk modunu kullan**: Bu seçenek belirlendiğinde, hata ayıklayıcı yeni yerel hata ayıklayıcı yerine Visual Studio 2010 yerel hata ayıklayıcısını kullanır.

- Yeni hata ayıklama altyapısı .NET C++ C++ ifadeleri değerlendirmeyi desteklemediğinden, .net Code hata ayıklaması yaparken bu seçeneği kullanın. Ancak, yerel uyumluluk modunu etkinleştirmek, geçerli hata ayıklayıcı uygulamasına bağımlı birçok özelliği çalışır şekilde devre dışı bırakır. Örneğin, eski altyapıda Visual Studio 2015 projelerinde gibi `std::string` yerleşik türler için birçok Görselleştiriciler yoktur.   Bu durumlarda en iyi hata ayıklama deneyimi için Visual Studio 2013 projelerini kullanın.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da hata ayıklama](../debugger/index.md)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
