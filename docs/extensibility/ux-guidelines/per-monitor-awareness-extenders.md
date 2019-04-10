---
title: Visual Studio Genişleticileri İzleyici başına tanıma desteği
titleSuffix: ''
description: Her İzleyici-tanıma Visual Studio 2019 içinde kullanılabilir yeni genişletici desteği hakkında bilgi edinin.
ms.date: 04/09/2019
helpviewer_keywords:
- Visual Studio, PMA, per-monitor-awareness, extenders, Windows Forms
- Per-Monitor Awareness support for extenders
ms.assetid: ''
author: rub8n
ms.author: rurios
manager: anthc
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.topic: reference
ms.workload:
- multiple
ms.openlocfilehash: 42de73a29e053066c0fbeca72ca3511b58b2fa7e
ms.sourcegitcommit: 0a2fdc23faee77187e10a1c19665ba5a1ac68e72
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/10/2019
ms.locfileid: "59477813"
---
# <a name="per-monitor-awareness-support-for-visual-studio-extenders"></a>Visual Studio Genişleticileri İzleyici başına tanıma desteği

Visual Studio 2019 önceki sürümler DPI tanıma bağlamları sistem kullanan yerine bir izleyici başına DPI kullanan (PMA) ayarlama sahipti. Farkındalık sonuçlandı sistemde çalışan düzeyi düşürülmüş bir görsel deneyimi (örneğin bulanık yazı tipleri veya simgeler) Visual Studio her farklı ölçek Etkenler değerlerine sahip işlemek zorunda veya uzaktan oturum açın (örneğin farklı farklı ekranı yapılandırmaları ile makineleri Windows) ölçeklendirme.

Visual Studio 2019 DPI tanıma bağlamı olarak İzleyici başına kullanan, sağlayarak hizmetin barındırıldığı görünen yapılandırmasına göre işlemek için Visual Studio kümesi yerine genel sistem tarafından tanımlanan yapılandırma ' dir. Sonuçta PMA desteği uygulayan yüzey alanlar için NET bir kullanıcı Arabirimi içinde çevirme.

Başvurmak [Windows üzerinde yüksek DPI Masaüstü uygulama geliştirme](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows) hüküm ve genel senaryo hakkında daha fazla bilgi için bu belgede ele.

## <a name="quickstart"></a>Hızlı başlangıç
- Visual Studio PMA modunda çalıştığından emin olun (bkz **etkinleştirme PMA**)

- Uzantı çalışır, bir dizi ortak senaryolar arasında doğru doğrulamak (bkz **uzantılarınızı PMA sorunlarıyla ilgili test**)

- Sorunlar bulursanız, yeni PMA nugget paketini eklemek için Stratejiler ve bu belgede ele alınan öneriler kullanarak sorunları tanılayıp

## <a name="enabling-pma"></a>PMA etkinleştirme
Visual Studio'da PMA etkinleştirmek için aşağıdaki gereksinimlerin karşılanması gerekir:
1)  Windows 10 Nisan 2018 Güncelleştirmesi (v1803 RS4) veya üzeri
2)  .NET framework 4.8 RTM veya üzeri (şu anda Önizleme tek başına veya son paketle birlikte Windows Insider derlemeleri)
3)  Visual Studio 2019 ile ["Farklı piksel densities ekranlar için Optimize işleme"](https://docs.microsoft.com/visualstudio/ide/reference/general-environment-options-dialog-box?view=vs-2019) seçeneği etkin

Bu gereksinimlerin karşılanıp karşılanmadığından sonra Visual Studio PMA süreci boyunca otomatik olarak etkinleştirir.

## <a name="testing-your-extensions-for-pma-issues"></a>Uzantılarınızı PMA sorunlar için test etme

Visual Studio resmi olarak WPF, Windows Forms, Win32 ve HTML/JS UI çerçeveleri destekler. Visual Studio PMA moduna geçirdiğinizde, farklı kullanıcı Arabirimi yığınları farklı davranır. Bu nedenle, UI Çerçevesi'ne olursa olsun tüm kullanıcı Arabirimi PMA ile uyumlu olduğundan emin olmak için bir test geçişi gerçekleştirilir önerilir.

UI çerçevesi bağımsız olarak uzantınızı destekler, aşağıdaki yaygın senaryoları doğrulamak önerilir:

1. Uygulamanın çalışmasını * durumdayken ölçek faktörü tek bir izleme ortamı değiştirme
    - Bu senaryoda kullanıcı arabirimini dinamik olarak Windows DPI değiştirilmesi yanıt verdiğini test yardımcı olur.

2. Takma/çıkarma işlemlerini uygulama çalışırken eklenmiş bir izleyici için birincil ve ekli İzleyici ayarlandığı bir dizüstü bilgisayar, bir farklı ölçek faktörü birincil daha vardır.
    - Bu senaryo DPI değişiklik yanı sıra görüntüler dinamik olarak işleme eklendi veya kaldırılmasını kullanıcı Arabirimi ekranı için yanıt verdiğini test yardımcı olur.

3. Birden çok monitör farklı ölçek faktörleri sahip olmak ve bunlar arasında uygulama taşıma.
    - Bu senaryo için görüntü DPI değişikliği UI yanıt verdiğini test yardımcı olur.
    
4. Uzak bir makine yerel ve uzak makineler için birincil İzleyici farklı ölçek Etkenler olduğunda.
    - Bu senaryoda kullanıcı arabirimini dinamik olarak Windows DPI değiştirilmesi yanıt verdiğini test yardımcı olur.

Olup olmadığı ya da kod yararlanır olup UI sorunlar yaşayabilirsiniz için iyi bir başlangıç sınama olduğu *Microsoft.VisualStudio.Utilities.Dpi.DpiHelper* veya *Microsoft.VisualStudio.PlatformUI.DpiHelper* sınıfları. Bu eski DpiHelper sınıfları yalnızca sistem DPI tanıma destekler ve işlem PMA olduğunda her zaman doğru şekilde çalışmaz.

Bu DpiHelpers tipik kullanımını şöyle görünecektir:

```cs
Point screenTopRight = logicalBounds.TopRight.LogicalToDeviceUnits();

POINT screenIntTopRight = new POINT
{
    x = (int)screenTopRIght.X,
    y = (int)screenTopRIght.Y
}

IntPtr monitor = NativeMethods.MonitorFromPoint(screenIntTopRight, NativeMethods.Monitor_DEFAULTTONEARST);
```

Önceki örnekte, böylece doğru İzleyici işaretçi geri döndürmek için cihaz koordinatları bekliyor MonitorFromPoint yerel yönteme geçirilen pencerenin mantıksal sınırları temsil eden bir dikdörtgen cihaz birimlerine dönüştürülür.

### <a name="classes-of-issues"></a>Sorunların sınıfları

Visual Studio için PMA etkin olduğunda, kullanıcı Arabirimi sorunları birkaç yaygın şekilde çoğaltabilirsiniz. En değilse, bu konunun Visual Studios desteklenen UI çerçeveleri hiçbirinde oluşabilir. Ayrıca, bu sorunları bile zaman kullanıcı arabiriminin bir parça içinde karma mod DPI senaryolarında ölçeklendirme yapılıyorsa oluşabilir (Windows için başvuru [belgeleri](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows) daha fazla bilgi için). 

#### <a name="win32-window-creation"></a>Win32 pencere oluşturma
Windows CreateWindow() veya CreateWindowEx() oluştururken, yaygın bir düzen olduğunu penceresinde koordinatları 0,0 (birincil ekranın sol üst köşesinde), oluşturulacak ardından taşıyın son konumuna. Ancak, bir DPI tetiklemek pencerenin neden olabilir, böylece ileti veya diğer UI iletilerini veya olaylar yeniden Tetikle ve sonunda istenmeyen davranışlara veya işleme neden, olay değiştirildi.

#### <a name="wpf-element-placement"></a>WPF öğesi yerleştirme
Öğeleri birincil olmayan DPI durumda olduğunda eski Microsoft.VisualStudio.Utilities.Dpi.DpiHelper kullanarak WPF öğeleri taşırken, sol üst koordinat doğru şekilde hesaplanmış olabilir değil.

#### <a name="serialization-of-ui-element-sizes-or-positions"></a>Kullanıcı Arabirimi öğesi boyutları veya konumlarını serileştirilmesi
Hangi konumunda depolanmış değerinden farklı bir DPI bağlama sırasında kullanıcı Arabirimi boyut ve konum geri yüklendiğinde, konumlandırılır ve boyutu yanlış. Bunun nedeni, böylece doğru İzleyici işaretçi geri döndürmek için cihaz koordinatları bekliyor MonitorFromPoint Win32 yönteme geçirilen pencerenin mantıksal sınırları cihaz birimlerine dönüştürülür kullanmasıdır.

#### <a name="incorrect-scaling"></a>Yanlış ölçeklendirme
Birincil DPI üzerinde oluşturulan UI öğeleri, ancak farklı DPI bir ekran için taşınmış, yeniden ölçeklendirmek yok ve bu nedenle, çok büyük veya çok küçük olan yukarı içeriklerini sona erer doğru bir şekilde ölçeklendirilir.

#### <a name="incorrect-bounding"></a>Yanlış sınırlayıcı
Benzer şekilde, birincil olmayan DPI olarak takıldığında, yeni sınırları doğru şekilde hesaplanacak olmaz ancak ölçeklendirme sorunu için kullanıcı Arabirimi öğeleri doğru birincil DPI bağlamları kendi sınır hesaplar. Bu nedenle, içerik penceresi çok küçük veya çok büyük boşluk veya kırpma sonuçları barındırma UI ile karşılaştırıldığında olur.

#### <a name="drag--drop"></a>Sürükle & bırak
Zaman içinde karma mod DPI senaryolarında (hem birincil hem de birincil olmayan DPI bağlamda işleme örneğin farklı kullanıcı Arabirimi öğeleri), sürükle ve bırak koordinatları, yanlış'kurmak son bırakma konumu sonuçta elde edilen işlemi.

#### <a name="out-of-process-ui"></a>İşlem dışı kullanıcı Arabirimi
İşlem dışı bazı kullanıcı Arabirimi oluşturulur ve dış oluşturma işlemi, Visual Studio daha farklı bir DPI tanıma modda ise, bunu herhangi bir önceki işleme sorunlarını ortaya çıkarabilir.

#### <a name="windows-forms-controls-images-or-windows-not-displaying"></a>Windows Forms denetimleri, görüntüleri veya windows görünmüyor
Bu sorunun temel nedeni bir denetim veya farklı bir DpiAwarenessContext penceresine bir DpiAwarenessContext penceresiyle yeniden üst öğe yap göndermeye çalışan geliştiricilere biridir. 

İş parçacığı davranışı barındırma açıkça değiştirilmediği sürece aşağıdaki resimler geçerli Windows işletim sistemi kısıtlamaları windows, üst öğe oluşturma göster:

![Ekran görüntüsü doğru ana öğe davranışı](../../extensibility/ux-guidelines/media/PMA-parenting-behavior.PNG)

Sonuç olarak, desteklenmeyen modları arasında üst-alt ilişkisi başarısız olur ve denetim veya penceresi beklenen şekilde çizilebilir değil.

### <a name="diagnosing-issues"></a>Sorunları tanılama
PMA ilişkili sorunları tanımlamak için kullanıldığında dikkate alınması gereken birçok faktör vardır: 

1. Kullanıcı Arabirimi veya beklenen API mantıksal veya cihaz değerleri.
    - WPF kullanıcı Arabirimi ve API'ler genellikle mantıksal değerleri kullanılır (ama her zaman kullanılmaz)
    - Win32 UI ve API'ler genellikle cihaz değerleri kullanın

2. Burada değerlerin nereden geldiğini?
    - Diğer kullanıcı Arabirimi veya API değerlerini alma, cihaz geçirme veya mantıksal değer olur.
    - Birden fazla kaynaktan değerleri almaya, hepsi kullanın/aynı türde değerler bekliyorsunuz veya dönüştürmeler karışık ve eşleşmesi gerekiyor mu?

3. UI sabitleri kullanımda ve hangi biçimindedir, bunlar misiniz?

4. İş parçacığı değerleri için doğru DPI bağlamı, alıyor?
    - Genellikle kod yollarını CLMM etkinleştirmek için değişiklikleri doğru bağlamda koymanız gerekir, ancak ana ileti döngüsü veya olay akışı dışında çalışmanın yanlış DPI bağlamda paralellikle çalışabilir.

5. Değerleri DPI bağlam sınırlarını aşan?
    - Sürükle ve bırak koordinatları DPI bağlamları burada çapraz ortak bir durumda olur. Penceresi doğru şeyleri yapacakları dener, ancak bazı durumlarda, eşleşen bağlam sınırlarını emin olmak için dönüştürme işi yapmak kullanıcı Arabirimi konak gerekebilir.

### <a name="pma-nugget-package"></a>PMA Nugget paket
Yeni DpiAwarness kitaplıkları Microsoft.VisualStudio.DpiAwareness NuGet paketi bulunamadı.

### <a name="recommended-tools"></a>Önerilen Araçlar
Aşağıdaki araçlar, Visual Studio tarafından desteklenen farklı kullanıcı Arabirimi yığınları bazıları arasında PMA ile ilgili sorunlar hata ayıklama yardımcı olabilir.

#### <a name="snoop"></a>Gözetleme
Gözetleme yerleşik Visual Studio XAML araçlar yoksa bazı fazladan işlevsellik olan bir XAML hata ayıklama aracıdır. Ayrıca, gözetleme etkin bir şekilde görüntüleyin ve onun bir WPF UI ince ayar yapmak için Visual Studio hata ayıklama gerekmez. Gözetleme PMA sorunları tanılamak için yararlı olabilir başlıca iki yolu olduğunu doğrulamak için mantıksal yerleştirme koordinatları veya boyut sınırları ve doğrulamak için kullanıcı Arabirimi doğru DPI vardır.
 
#### <a name="visual-studio-xaml-tools"></a>Visual Studio XAML araçları
Gözetleme gibi Visual Studio'da XAML Araçlar PMA sorunları tanılamanıza yardımcı olabilir. Büyük olasılıkla sorunlu bulunduktan sonra kesme noktaları ayarlayın ve hata ayıklama pencerelerinde yanı sıra Canlı görsel ağaç pencerenin UI sınırları ve geçerli DPI incelemek için kullanın.

## <a name="strategies-for-fixing-pma-issues"></a>PMA sorunlarını giderme stratejileri

### <a name="replacing-dpihelper-calls"></a>DpiHelper çağrıları değiştirme
Çoğu durumda, UI sorumlarını PMA içinde eski yönetilen kodda çağrısına değiştirmek için boils: *Microsoft.VisualStudio.Utilities.Dpi.DpiHelper* ve *Microsoft.VisualStudio.PlatformUI.DpiHelper* sınıflarıyla yeni çağrıları *Microsoft.VisualStudio.Utilities.DpiAwareness* yardımcı sınıfı. 

Yerel kod için eski değiştirilmesini çağrıları gerektirdiği *VsUI::CDpiHelper* sınıfı ile yeni çağrıları *VsUI::CDpiAwareness* sınıfı. DpiHelper sınıfları, ek bir giriş parametresi ancak gereksinim duyduğunuz kadar yeni DpiAwareness ve CDpiAwareness sınıfları aynı dönüştürme sağla: dönüştürme işlemi için bir başvuru olarak kullanmak için kullanıcı Arabirimi öğesi. 

Yönetilen DpiAwareness sınıfı Yardımcıları WPF görseller, Windows Forms denetimleri ve Win32 Cwnd'lerden ve HMONITORs (hem de IntPtrs biçiminde), yerel CDpiAwareness sınıfı teklifler HWND ve HMONITOR Yardımcıları sırasında sunar.

### <a name="windows-forms-dialogs-windows-or-controls-displayed-in-the-wrong-dpiawarenesscontext"></a>Windows Forms iletişim kutuları, windows veya yanlış DpiAwarenessContext içinde görüntülenen denetimleri
Hatta bir başarılı ana öğe farklı DpiAwarenessContext (nedeniyle windows varsayılan davranış) ile Windows sonra kullanıcılar farklı DpiAwarenessContext windows farklı şekilde artırıp azaltırken sorunları ölçeklendirme yine de görebilirsiniz. Sonuç olarak, kullanıcıların kullanıcı Arabirimi üzerindeki hizalama/bulanık metin veya görüntü sorunları görebilirsiniz.

Uygulama tüm windows ve denetimler için doğru DpiAwarenessContext kapsamını ayarlamak için kullanılan çözümüdür.

### <a name="tlmm-dialogs"></a>TLMM iletişim kutuları
Kalıcı iletişim kutuları gibi üst düzey pencerelere oluştururken, iş parçacığı oluşturulan HWND önce doğru durumda olduğundan emin olmak önemlidir. İş parçacığı tarafından sistem tanıma içine yerel CDpiScope Yardımcısını kullanarak dahil edilebilir veya DpiAwareness.EnterDpiScope yardımcı yönetilebilir. (TLMM WPF olmayan iletişim kutuları/Windows'da genelde kullanılmalıdır.)

### <a name="child-level-mixed-mode-clmm"></a>Alt düzey karma mod (CLMM)

Varsayılan olarak, alt öğe pencerelerini ebeveynleri olarak aynı DPI tanıma modunu alır. Ancak, SetThreadDpiHostingBehavior geçersiz kılmak için kullanabileceğiniz ve alt pencereler, üst veya ana bilgisayar farklı bir ölçeklendirme modu çalıştırmak sahip.


#### <a name="clmm-issues"></a>CLMM sorunları
Ana ileti döngüsü veya olay zinciri kapsamında gerçekleşen UI hesaplama yapacaklarımızın sonuna doğru DPI bağlamı zaten çalıştırıyor olmalıdır. Ancak, gibi (boşta kalma süresi görev sırasında veya kullanıcı Arabirimi iş parçacığı kapalı, ardından geçerli DPI bağlamı için kullanıcı Arabirimi misplacement başta veya sorunları yanlış boyutlandırma yanlış olabilir. koordinat veya boyutlandırma hesaplamalar ana bu iş akışları dışında yapılması durumunda İş parçacığının doğru kullanıcı Arabiriminde alternatifin iş genel sorunu giderir.
 
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
```cplusplus
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

**NOT**: Visual Studio yalnızca PerMonitorV2 tanıma destekler, böylece PerMonitor sabit listesi değeri DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 Windows değerine çevirir.

## <a name="known-issues"></a>Bilinen sorunlar

### <a name="windows-forms"></a>Windows Forms

Yeni Karma mod senaryolar için en iyi duruma getirmek için Windows Forms, üst açıkça ayarlanmadı her nasıl denetimleri ve windows oluşturur değiştirildi. Daha önce açık bir üst olmadan denetimlere bir iç "park penceresi" geçici bir üst denetim ya da oluşturulan penceresi olarak kullanılır. 

"Park penceresi" altında uygulama çalışan işlemi kendi DpiAwarenessContext alır. Denetim park penceresi olarak aynı DpiAwarenessContext devralır ve ardından özgün ve beklenen üst uygulama geliştiricisi tarafından öğelerinin yeniden üst öğesi.  Hedeflenen üst denetime oluşturulan denetimi olarak aynı DpiAwarenessContext olmadığında çalışmaz.

İtibariyle .NET 4.8, üst denetim veya penceresi açıkça ayarlanmadı Windows Forms park denetimi veya pencere oluşturma istendiği iş parçacığının DpiAwarenessContext eşleşen pencere için bir sorgu ve, geçici bir üst öğe olarak kullanabilirsiniz. Diğer bir deyişle, oluşturulduktan sonra Denetim artık hedeflenen DpiAwarenessContext ile oluşturulur. Denetim veya pencere sonra beklenen üst uygulama geliştiricisi tarafından öğelerinin yeniden üst öğesi.
