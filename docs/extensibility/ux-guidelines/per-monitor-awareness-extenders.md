---
title: Visual Studio Genişleticileri İzleyici başına tanıma desteği
titleSuffix: ''
description: Her İzleyici-tanıma Visual Studio 2019 içinde kullanılabilir yeni genişletici desteği hakkında bilgi edinin.
ms.date: 04/10/2019
helpviewer_keywords:
- Visual Studio, PMA, per-monitor-awareness, extenders, Windows Forms
- Per-Monitor Awareness support for extenders
ms.assetid: ''
author: rub8n
ms.author: rurios
manager: anthc
ms.prod: visual-studio-windows
monikerRange: vs-2019
ms.technology: vs-ide-general
ms.topic: reference
ms.workload:
- multiple
ms.openlocfilehash: 44938c5753491521702867398a514f770cf831fb
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60099396"
---
# <a name="per-monitor-awareness-support-for-visual-studio-extenders"></a>Visual Studio Genişleticileri İzleyici başına tanıma desteği
Visual Studio 2019 önceki sürümler, Sistem İzleyici başına DPI kullanan (PMA) yerine uyumlu olarak DPI tanıma bağlamları vardı. Düzeyi düşürülmüş bir görselde sonuçlanan sistem tanıma çalışan farklı ölçek Etkenler veya uzaktan değerlerine sahip farklı bir ekranı yapılandırmaları ile makinelere örneğin (farklı işlemek Visual Studio sahip olduğunda (örneğin bulanık yazı tipleri veya simgeler) deneyimi Windows) ölçeklendirme.

Ortamı, bir tek sistem tanımlı yapılandırması yerine Visual Studio hizmetin barındırıldığı görünen yapılandırmasına göre işlemek için izin verme desteklediğinde, Visual Studio 2019 DPI tanıma bağlamında PMA ayarlanır. Sonuçta PMA modu desteği yüzey alanlarda her zaman NET bir UI içine çevirme.

Başvurmak [Windows üzerinde yüksek DPI Masaüstü uygulama geliştirme](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows) hüküm ve genel senaryo hakkında daha fazla bilgi için bu belgede ele.

## <a name="quickstart"></a>Hızlı başlangıç
- Visual Studio PMA modunda çalıştığından emin olun (bkz **etkinleştirme PMA**)

- Uzantı çalışır, bir dizi ortak senaryolar arasında doğru doğrulamak (bkz **uzantılarınızı PMA sorunlarıyla ilgili test**)

- Bir sorunla karşılaşmanız halinde, bu sorunları tanılayıp bu belgede ele alınan stratejileri/önerileri kullanabilirsiniz. Ayrıca yeni eklemeniz gerekir [Microsoft.VisualStudio.DpiAwareness](https://www.nuget.org/packages/Microsoft.VisualStudio.DpiAwareness/) NuGet paketini projenize gerekli API'lerine erişmek için.

## <a name="enabling-pma"></a>PMA etkinleştirme
Visual Studio'da PMA etkinleştirmek için aşağıdaki gereksinimlerin karşılanması gerekir:
1) Windows 10 Nisan 2018 Güncelleştirmesi (v1803 RS4) veya üzeri
2) .NET framework 4.8 RTM veya üzeri
3) Visual Studio 2019 ile ["Farklı piksel densities ekranlar için Optimize işleme"](https://docs.microsoft.com/visualstudio/ide/reference/general-environment-options-dialog-box?view=vs-2019) seçeneği etkin

Bu gereksinimlerin karşılanıp karşılanmadığından sonra Visual Studio süreci boyunca PMA modu otomatik olarak etkinleştirir.

> [!NOTE]
> Visual Studio 2019 güncelleştirme #1 olduğunda, Windows Forms içerik (örneğin, özellik tarayıcısı) vs'de PMA destekleyecektir.

## <a name="testing-your-extensions-for-pma-issues"></a>Uzantılarınızı PMA sorunlar için test etme

Visual Studio resmi olarak WPF, Windows Forms, Win32 ve HTML/JS UI çerçeveleri destekler. Visual Studio PMA moduna geçirdiğinizde, her bir kullanıcı Arabirimi yığında farklı davranır. Bu nedenle, UI Çerçevesi'ne olursa olsun tüm kullanıcı Arabirimi PMA modu ile uyumlu olduğundan emin olmak için bir test geçişi gerçekleştirilir önerilir.

Aşağıdaki senaryoları doğrulamak önerilir:

1. Uygulamanın çalışmasını * durumdayken ölçek faktörü tek bir izleme ortamı değiştirme
    - Bu senaryoda kullanıcı arabirimini dinamik olarak Windows DPI değiştirilmesi yanıt verdiğini test yardımcı olur.

2. Yerleştirme/burada birincil siteye bağlı bir izleyici ayarlanır ve uygulama çalışırken bir farklı ölçek faktörü dizüstü daha eklenen monitör sahip bir dizüstü desteklemiyor.
    - Bu senaryo DPI değişiklik yanı sıra görüntüler dinamik olarak işleme eklendi veya kaldırılmasını kullanıcı Arabirimi ekranı için yanıt verdiğini test yardımcı olur.

3. Birden çok monitör farklı ölçek faktörleri sahip olmak ve bunlar arasında uygulama taşıma.
    - Bu senaryo için görüntü DPI değişikliği UI yanıt verdiğini test yardımcı olur.
    
4. Uzak bir makine yerel ve uzak makineler için birincil İzleyici farklı ölçek Etkenler olduğunda.
    - Bu senaryoda kullanıcı arabirimini dinamik olarak Windows DPI değiştirilmesi yanıt verdiğini test yardımcı olur.

Kod mi yararlanır olup, kullanıcı Arabirimi sorunlar yaşayabilirsiniz için iyi bir başlangıç sınama olduğu *Microsoft.VisualStudio.Utilities.Dpi.DpiHelper*, *Microsoft.VisualStudio.PlatformUI.DpiHelper*, veya *VsUI::CDpiHelper* sınıfları. Bu eski DpiHelper sınıfları yalnızca sistem DPI tanıma destekler ve işlem PMA olduğunda her zaman doğru şekilde çalışmaz.

Bu DpiHelpers tipik kullanımını şöyle görünecektir:

```cs
Point screenTopRight = logicalBounds.TopRight.LogicalToDeviceUnits();

POINT screenIntTopRight = new POINT
{
    x = (int)screenTopRIght.X,
    y = (int)screenTopRIght.Y
}

// Declared via P/Invoke
IntPtr monitor = MonitorFromPoint(screenIntTopRight, MONITOR_DEFAULTTONEARST);
```

Önceki örnekte, böylece doğru İzleyici işaretçi geri döndürmek için cihaz koordinatları bekliyor MonitorFromPoint yerel yönteme geçirilen pencerenin mantıksal sınırları temsil eden bir dikdörtgen cihaz birimlerine dönüştürülür.

### <a name="classes-of-issues"></a>Sorunların sınıfları
Visual Studio için PMA modu etkin olduğunda, kullanıcı Arabirimi sorunları birkaç yaygın şekilde çoğaltabilirsiniz. Bu konular hakkında en değilse, Visual Studio'nun desteklenen UI çerçeveleri hiçbirinde oluşabilir. Kullanıcı arabiriminin bir parça içinde karma mod DPI senaryolarında ölçeklendirme barındırıldığında ek olarak, bu sorunları da oluşabilir (Windows için başvuru [belgeleri](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows) daha fazla bilgi için). 

#### <a name="win32-window-creation"></a>Win32 pencere oluşturma
Windows CreateWindow() veya CreateWindowEx() oluştururken, yaygın bir düzen pencere (0,0) koordinatlarda oluşturmaktır (birincil ekranın sol üst köşesinde), ardından son konumuna taşıyın. Ancak, bir DPI tetiklemek pencerenin neden olabilir, böylece ileti veya diğer UI iletilerini veya olaylar yeniden Tetikle ve sonunda istenmeyen davranışlara veya işleme neden, olay değiştirildi.

#### <a name="wpf-element-placement"></a>WPF öğesi yerleştirme
Öğeleri bir birincil olmayan DPI üzerinde olduğunda eski Microsoft.VisualStudio.Utilities.Dpi.DpiHelper kullanarak WPF öğeleri taşırken, sol üst koordinat doğru şekilde hesaplanmış olabilir değil.

#### <a name="serialization-of-ui-element-sizes-or-positions"></a>Kullanıcı Arabirimi öğesi boyutları veya konumlarını serileştirilmesi
Hangi konumunda depolanmış değerinden farklı bir DPI bağlama sırasında kullanıcı Arabirimi boyut ve konum (cihaz birimleri kaydettiyseniz) geri yüklendiğinde, konumlandırılır ve boyutu yanlış. Devralınmış bir DPI ilişki cihaz birimlerine sahip olur.

#### <a name="incorrect-scaling"></a>Yanlış ölçeklendirme
Birincil DPI üzerinde oluşturulan UI öğeleri, ancak farklı DPI bir ekran için taşınmış, yeniden ölçeklendirmek yok ve bu nedenle, çok büyük veya çok küçük olan yukarı içeriklerini sona erer doğru bir şekilde ölçeklendirilir.

#### <a name="incorrect-bounding"></a>Yanlış sınırlayıcı
Benzer şekilde, birincil olmayan DPI olarak takıldığında, yeni sınırları doğru şekilde hesaplanacak olmaz ancak ölçeklendirme sorunu için kullanıcı Arabirimi öğeleri doğru birincil DPI bağlamları kendi sınır hesaplar. Bu nedenle, içerik penceresi çok küçük veya çok büyük boşluk veya kırpma sonuçları barındırma UI ile karşılaştırıldığında olur.

#### <a name="drag--drop"></a>Sürükle & bırak
Zaman içinde karma mod DPI senaryolarında (farklı DPI tanıma modda işleme örneğin farklı kullanıcı Arabirimi öğeleri), sürükle ve bırak koordinatları, yanlış'kurmak son bırakma konumu sonuçta elde edilen işlemi.

#### <a name="out-of-process-ui"></a>İşlem dışı kullanıcı Arabirimi
İşlem dışı bazı kullanıcı Arabirimi oluşturulur ve dış oluşturma işlemi, Visual Studio daha farklı bir DPI tanıma modda ise, bunu herhangi bir önceki işleme sorunlarını ortaya çıkarabilir.

#### <a name="windows-forms-controls-images-or-layouts-rendered-incorrectly"></a>Windows Forms denetimleri, görüntüleri veya yanlış işlenen düzenleri
Tüm Windows Formları içeriği PMA modunu destekler. Sonuç olarak, yanlış düzenleri sorun işleme veya ölçeklendirme görebilirsiniz. Olası bir çözüm "Sistem tanıma" DpiAwarenessContext Windows Forms içeriğinde açıkça işlemek için bu durumda, (başvurmak [bir denetimi ile belirli bir DpiAwarenessContext zorlama](#forcing-a-control-into-a-specific-dpiawarenesscontext)).

#### <a name="windows-forms-controls-or-windows-not-displaying"></a>Windows Forms denetimleri veya windows görünmüyor
Bu sorunun temel nedeni bir denetim veya farklı bir DpiAwarenessContext ile bir pencere için bir DpiAwarenessContext penceresiyle yeniden üst öğe yap göndermeye çalışan geliştiricilere biridir.

Aşağıdaki resim Göster geçerli **varsayılan** windows üst öğe oluşturma, Windows işletim sistemi kısıtlamaları:

![Ekran görüntüsü doğru ana öğe davranışı](../../extensibility/ux-guidelines/media/PMA-parenting-behavior.PNG)

> [!Note]
> İş parçacığı barındırma davranışı ayarlayarak bu davranışı değiştirebilirsiniz (bkz [DpiHostinBehaviour](https://docs.microsoft.com/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior)).

Sonuç olarak, desteklenmeyen modları arasında üst-alt ilişkisi başarısız olur ve denetim veya penceresi beklenen şekilde çizilebilir değil.

### <a name="diagnosing-issues"></a>Sorunları tanılama
PMA ilişkili sorunları tanımlamak için kullanıldığında dikkate alınması gereken birçok faktör vardır: 

1. Kullanıcı Arabirimi veya mantıksal beklediğiniz API yoksa veya cihaz değerleri.
    - WPF kullanıcı Arabirimi ve API'ler genellikle mantıksal değerleri kullanılır (ama her zaman kullanılmaz)
    - Win32 UI ve API'ler genellikle cihaz değerleri kullanın

2. Burada değerlerin nereden geldiğini?
    - Diğer kullanıcı Arabirimi veya API değerlerini alma, cihaz geçirme veya mantıksal değer olur.
    - Birden fazla kaynaktan değerleri almaya, hepsi kullanın/aynı türde değerler bekliyorsunuz veya dönüştürmeler karışık ve eşleşmesi gerekiyor mu?

3. UI sabitleri kullanımda ve hangi biçimindedir, bunlar misiniz?

4. İş parçacığı değerleri için doğru DPI bağlamı, alıyor?
    - Genellikle kod yollarını karma DPI barındırmayı etkinleştirmek için değişiklikleri doğru bağlamda koymanız gerekir, ancak ana ileti döngüsü veya olay akışı dışında çalışmanın yanlış DPI bağlamda paralellikle çalışabilir.

5. Değerleri DPI bağlam sınırlarını aşan?
    - Sürükle ve bırak koordinatları DPI bağlamları burada çapraz ortak bir durumda olur. Penceresi doğru şeyleri yapacakları dener, ancak bazı durumlarda, eşleşen bağlam sınırlarını emin olmak için dönüştürme işi yapmak kullanıcı Arabirimi konak gerekebilir.

### <a name="pma-nuget-package"></a>PMA NuGet paketi
Yeni DpiAwarness kitaplıkları bulunabilir [Microsoft.VisualStudio.DpiAwareness](https://www.nuget.org/packages/Microsoft.VisualStudio.DpiAwareness/) NuGet paketi.

### <a name="recommended-tools"></a>Önerilen Araçlar
Aşağıdaki araçlar, Visual Studio tarafından desteklenen farklı kullanıcı Arabirimi yığınları bazıları arasında PMA ile ilgili sorunlar hata ayıklama yardımcı olabilir.

#### <a name="snoop"></a>Gözetleme
Gözetleme yerleşik Visual Studio XAML araçlar yoksa bazı fazladan işlevsellik olan bir XAML hata ayıklama aracıdır. Ayrıca, gözetleme etkin bir şekilde görüntüleyin ve onun bir WPF UI ince ayar yapmak için Visual Studio hata ayıklama gerekmez. Gözetleme PMA sorunları tanılamak için yararlı olabilir başlıca iki yolu olduğunu doğrulamak için mantıksal yerleştirme koordinatları veya boyut sınırları ve doğrulamak için kullanıcı Arabirimi doğru DPI vardır.
 
#### <a name="visual-studio-xaml-tools"></a>Visual Studio XAML araçları
Gözetleme gibi Visual Studio'da XAML Araçlar PMA sorunları tanılamanıza yardımcı olabilir. Büyük olasılıkla sorunlu bulunduktan sonra kesme noktaları ayarlayın ve hata ayıklama pencerelerinde yanı sıra Canlı görsel ağaç pencerenin UI sınırları ve geçerli DPI incelemek için kullanın.

## <a name="strategies-for-fixing-pma-issues"></a>PMA sorunlarını giderme stratejileri
### <a name="replacing-dpihelper-calls"></a>DpiHelper çağrıları değiştirme
Çoğu durumda, kullanıcı Arabirimi sorunlarını giderme PMA modunda boils eski yönetilen kodda çağrısına değiştirmek için *Microsoft.VisualStudio.Utilities.Dpi.DpiHelper* ve *Microsoft.VisualStudio.PlatformUI.DpiHelper*sınıflarıyla yeni çağrıları *Microsoft.VisualStudio.Utilities.DpiAwareness* yardımcı sınıfı. 

```cs
// Remove this kind of use:
Point deviceTopLeft = new Point(window.Left, window.Top).LogicalToDeviceUnits();

// Replace with this use:
Point deviceTopLeft = window.LogicalToDevicePoint(new Point(window.Left, window.Top));
```

Yerel kod için eski değiştirilmesini çağrıları gerektirdiği *VsUI::CDpiHelper* sınıfı ile yeni çağrıları *VsUI::CDpiAwareness* sınıfı. 

```cpp
// Remove this kind of use:
int cx = VsUI::DpiHelper::LogicalToDeviceUnitsX(m_cxS);
int cy = VsUI::DpiHelper::LogicalToDeviceUnitsY(m_cyS);

// Replace with this use:
int cx = m_cxS;
int cy = m_cyS;
VsUI::CDpiAwareness::LogicalToDeviceUnitsX(m_hwnd, &cx);
VsUI::CDpiAwareness::LogicalToDeviceUnitsY(m_hwnd, &cy);
```

DpiHelper sınıfları, ek bir giriş parametresi ancak gereksinim duyduğunuz kadar yeni DpiAwareness ve CDpiAwareness sınıfları aynı birim dönüştürme sağla: dönüştürme işlemi için bir başvuru olarak kullanmak için kullanıcı Arabirimi öğesi. Görüntü ölçeklendirme Yardımcıları yeni DpiAwareness/CDpiAwareness Yardımcıları yok dikkat edin önemlidir ve gerekirse [Imageservice](https://docs.microsoft.com/visualstudio/extensibility/image-service-and-catalog?view=vs-2019) bunun yerine kullanılmalıdır.

Yönetilen DpiAwareness sınıfı Yardımcıları WPF görseller, Windows Forms denetimleri ve Win32 Cwnd'lerden ve HMONITORs (hem de IntPtrs biçiminde), yerel CDpiAwareness sınıfı teklifler HWND ve HMONITOR Yardımcıları sırasında sunar.

### <a name="windows-forms-dialogs-windows-or-controls-displayed-in-the-wrong-dpiawarenesscontext"></a>Windows Forms iletişim kutuları, windows veya yanlış DpiAwarenessContext içinde görüntülenen denetimleri
Hatta bir başarılı ana öğe farklı DpiAwarenessContexts (nedeniyle Windows varsayılan davranış) ile Windows sonra kullanıcılar ile farklı DpiAwarenessContexts ölçeklendirme windows sorunları farklı ölçeklendirme yine de görebilirsiniz. Sonuç olarak, kullanıcılar hizalama/bulanık metni veya görüntü sorunları kullanıcı arabiriminde.

Uygulama tüm windows ve denetimler için doğru DpiAwarenessContext kapsamını ayarlamak için kullanılan çözümüdür.

### <a name="top-level-mixed-mode-tlmm-dialogs"></a>Üst düzey karma mod (TLMM) iletişim kutuları
Kalıcı iletişim kutuları gibi üst düzey pencerelere oluştururken, pencerenin (ve tanıtıcısını) önce doğru durumda iş parçacığı oluşturuluyor emin olmak önemlidir. İş parçacığı tarafından sistem tanıma içine yerel CDpiScope Yardımcısını kullanarak dahil edilebilir veya DpiAwareness.EnterDpiScope yardımcı yönetilebilir. (TLMM WPF olmayan iletişim kutuları/Windows'da genelde kullanılmalıdır.)

### <a name="child-level-mixed-mode-clmm"></a>Alt düzey karma mod (CLMM)
Varsayılan olarak, alt öğe pencerelerini bir üst oluşturduysanız, geçerli iş parçacığı DPI tanıma bağlamı veya sahip bir üst oluşturulduğunda üst öğenin DPI tanıma bağlamı alır. Bir alt, üst farklı bir DPI tanıma bağlama oluşturmak için iş parçacığının istenen DPI tanıma bağlamına dahil edilebilir. Ardından alt üst oluşturulabilir ve el ile üst penceresine öğelerinin yeniden üst öğesi.

#### <a name="clmm-issues"></a>CLMM sorunları
Ana ileti döngüsü veya olay zinciri kapsamında gerçekleşen UI hesaplama yapacaklarımızın sonuna doğru DPI tanıma bağlamı zaten çalıştırıyor olmalıdır. Ancak, gibi (boşta kalma süresi görev sırasında veya kullanıcı Arabirimi iş parçacığı kapalı, ardından geçerli DPI tanıma bağlamı için kullanıcı Arabirimi misplacement başta veya sorunları yanlış boyutlandırma yanlış olabilir. koordinat veya boyutlandırma hesaplamalar ana bu iş akışları dışında yapılması durumunda İş parçacığının doğru kullanıcı Arabiriminde alternatifin iş genel sorunu giderir.
 
#### <a name="opting-out-of-clmm"></a>CLMM dışında seçim yapma
Tam PMA desteklemek için bir WPF olmayan araç penceresi geçiriliyorsa CLMM dışında bırakmak gerekir. Bunu yapmak için yeni bir arabirim uygulanması gerekir: IVsDpiAware.

C#:

```cs
[InterfaceType(ComInterfaceType.InterfaceIsIUnknown)]
public interface IVsDpiAeware
{
    [ComAliasName("Microsoft.VisualStudio.Shell.Interop.VSDPIMode")]
    uint Mode {get;}
}
```
 
C++:

```cpp
IVsDpiAware : public IUnknown
{
    public:
        HRRESULT STDMETHODCALLTYPE get_Mode(__RCP__out VSDPIMODE *dwMode);
};
```

Yönetilen diller için türetilen sınıfta bu arabirimi uygulayan için en iyi yeri olan *Microsoft.VisualStudio.Shell.ToolWindowPane*. İçin C++, uygulayan aynı sınıf bu arabirim uygulamak için en iyi yeri olan *Ivswindowpane* vsshell.h öğesinden.

Bir __VSDPIMODE arabirimde modu özelliği tarafından döndürülen değer olduğunu (ve içinde bir uint dönüştürme yönetilen):

```cs
enum __VSDPIMODE
{
    VSDM_Unaware    = 0x01,
    VSDM_System     = 0x02,
    VSDM_PerMonitor = 0x03,
}
```

- Araç penceresi 96 DPI işlemesi gerektiğini farkında anlamına gelir, Windows için tüm diğer monitörlerde ölçeklendirme işler. Biraz bulanık olan içeriği sonuç.
- Araç penceresi için birincil DPI işlemesi gerektiğini sistem DPI sms_ınbox_manager. Herhangi bir eşleşen DPI ekranıyla NET görünür ancak DPI farklı veya oturum sırasında değiştirir, Windows ölçeklendirme işleyecek ve biraz bulanık olacaktır.
- PerMonitor araç penceresi tüm ekranlarda tüm Dpı'larda işlemesi gerektiğini ve her DPI değişiklikleri anlamına gelir.

> [!NOTE]
> Visual Studio yalnızca PerMonitorV2 tanıma destekler, böylece PerMonitor sabit listesi değeri DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 Windows değerine çevirir.

#### <a name="forcing-a-control-into-a-specific-dpiawarenesscontext"></a>Bir denetimi ile belirli bir DpiAwarenessContext zorlama
PMA modunu destekleyecek şekilde güncelleştirilmesini değil eski kullanıcı Arabirimi Visual Studio PMA modunda çalışırken çalışmak için ince yine de gerekebilir. Bir düzeltme, kullanıcı Arabirimi içinde doğru DpiAwarenessContext oluşturulduğundan emin olmayı içerir. Kullanıcı Arabirimi içinde belirli bir DpiAwarenessContext zorlamak için aşağıdaki kodu DPI kapsamıyla girebilirsiniz:

C#:

```cs
using (DpiAwareness.EnterDpiScope(DpiAwarenessContext.SystemAware))
{
    Form form = new MyForm();
    form.ShowDialog();
}
```

C++:

```cpp
void MyClass::ShowDialog()
{
    VsUI::CDpiScope dpiScope(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE);
    HWND hwnd = ::CreateWindow(...);
}
```

> [!NOTE]
> DpiAwarenessContext zorlama yalnızca WPF UI ve üst düzey WPF iletişim kutuları üzerinde çalışır. WPF kullanıcı Arabirimi oluşturma içeriği WPF UI ağacına eklenir hemen sonra araç pencerelerini veya tasarımcıları, içinde barındırılması için olduğunda, geçerli işlemin DpiAwarenessContext dönüştürülür.

## <a name="known-issues"></a>Bilinen sorunlar
### <a name="windows-forms"></a>Windows Forms

Yeni Karma mod senaryolar için en iyi duruma getirmek için Windows Forms, üst açıkça ayarlanmadı her nasıl denetimleri ve windows oluşturur değiştirildi. Daha önce açık bir üst olmadan denetimlere bir iç "park penceresi" geçici bir üst denetim ya da oluşturulan penceresi olarak kullanılır. 

.NET 4.8 önce tek bir "park kendi DpiAwarenessContext geçerli iş parçacığı DPI tanıma bağlamdan pencerenin oluşturma zamanında aldığı pencere" vardı. Denetimin işleyicisi oluşturulduğunda ve son/beklenen üst uygulama geliştiricisi tarafından yeniden üst herhangi bir ana öğesiz denetimi park penceresi olarak aynı DpiAwarenessContext devralır. Son ana pencereyi daha yüksek bir DpiAwarenessContext "park penceresi" sahipse, bu zamanlama tabanlı hatalarına neden.

.NET 4.8'den itibaren artık karşılaşılan her DpiAwarenessContext bir "park penceresi" yoktur. Diğer bir önemli fark, denetimi oluşturulduğunda tanıtıcı oluşturulmadığında, denetim için kullanılan DpiAwarenessContext önbelleğe ' dir. Bu genel uç davranışını aynıdır, ancak tutarlı bir sorunu zamanlama tabanlı bir sorunla kullanılan ne kapatabilirsiniz anlamına gelir. Ayrıca uygulama geliştiricisinin daha kesin bir davranış, kullanıcı Arabirimi kodları yazmaya ve doğru bir şekilde kapsam için tanır.
