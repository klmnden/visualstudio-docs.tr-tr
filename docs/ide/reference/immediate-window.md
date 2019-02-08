---
title: Komut Penceresi
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
f1_keywords:
- VS.ImmediateWindow
helpviewer_keywords:
- design-time expression evaluation
- Immediate window
- first-chance exception notifications
ms.assetid: d33e7937-73f3-4c69-9df0-777a8713c6f2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3947c2f16be4e5c0d8054e48a46981aa22475423
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55931955"
---
# <a name="immediate-window"></a>Komut penceresi

**Hemen** penceresi, hata ayıklama ve ifadelerini değerlendirme, deyimleri yürütme, değişken değerlerini yazdırma vb. için kullanılır. Değerlendirilen veya hata ayıklama sırasında geliştirme dili tarafından yürütülen ifadeleri girmenizi sağlar.

Görüntülenecek **hemen** penceresinde düzenlemeye yönelik bir proje açın ve ardından **hata ayıklama** > **Windows** > **hemen**  veya basın **Ctrl**+**Alt**+**miyim**. Ayrıca girebilirsiniz **Debug.Immediate** içinde **komut** penceresi.

Kullanabileceğiniz **hemen** bireysel Visual Studio komutları için pencere. Kullanılabilir komutlar içeren `EvaluateStatement`, değerleri değişkenlere atamak için kullanılabilir. **Hemen** penceresi de IntelliSense'i destekler.

## <a name="display-the-values-of-variables"></a>Değişkenlerin değerlerini görüntüleme

**Hemen** penceresi özellikle kullanışlı olabilir bir uygulamanın hatalarını ayıklama sırasında. Örneğin, bir değişkenin değerini denetlemek için `varA`, kullanabileceğiniz [Yazdır komutu](../../ide/reference/print-command.md):

```cmd
>Debug.Print varA
```

Soru işareti (?) için bir diğer addır `Debug.Print`, bu komut ayrıca yazılabilir:

```cmd
>? varA
```

Bu komutun her iki sürümü değişken değerini döndürmek `varA`.

> [!TIP]
> Bir Visual Studio komut vermek için **hemen** penceresinde komutun önüne gerekir büyüktür işareti (>). Birden fazla komut girmek için geçin **komut** penceresi.

## <a name="design-time-expression-evaluation"></a>Tasarım zamanı ifade değerlendirmesi

Kullanabileceğiniz **hemen** tasarım zamanında bir işlev veya alt yordamı yürütmek için pencere.

### <a name="execute-a-function-at-design-time"></a>Tasarım zamanında bir işlevi yürütmek

1. Aşağıdaki kodu kopyalayın bir [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] konsol uygulaması:

   ```vb
   Module Module1

       Sub Main()
           MyFunction(5)
       End Sub

       Function MyFunction(ByVal input as Integer) As Integer
           Return input * 2
       End Function

   End Module
   ```

2. Üzerinde **hata ayıklama** menüsünü tıklatın **Windows**ve ardından **hemen**.

3. Tür `?MyFunction(2)` içinde **hemen** penceresi ve ENTER tuşuna **Enter**.

    **Hemen** penceresi çalıştıran `MyFunction` ve görüntüler `4`.

Visual Studio, işlev veya alt yordam bir kesme noktası içeriyorsa, uygun noktada yürütmeyi keser. Ardından, programınızın durumunu incelemek için hata ayıklayıcı penceresini kullanabilirsiniz. Daha fazla bilgi için [izlenecek yol: Tasarım zamanında hata ayıklama](../../debugger/walkthrough-debugging-at-design-time.md).

Bir yürütme ortamı gerektiren proje türlerinde tasarım zamanı ifade değerlendirmesi kullanamazsınız dahil olmak üzere [!INCLUDE[trprVSTOshort](../../ide/reference/includes/trprvstoshort_md.md)] projeleri, web projeleri, akıllı cihaz projeleri ve SQL projeleri.

### <a name="design-time-expression-evaluation-in-multi-project-solutions"></a>Çoklu proje çözümlerinde tasarım zamanı ifade değerlendirmesi

Tasarım zamanı ifade değerlendirmesi için bağlam sağlarken, Visual Studio Çözüm Gezgini'nde seçili olan projeye başvurur. Çözüm Gezgini'nde proje seçtiyseniz, Visual Studio Başlangıç projesine karşı işlevi değerlendirmeye çalışır. İşlev geçerli bağlamda değerlendirilemezse, bir hata iletisi alırsınız. Çözümün başlangıç projesi olmayan bir projede bir işlevi değerlendirmeye çalışıyorsanız ve bir hata alırsanız, Çözüm Gezgini'nde projeyi seçmeyi deneyin ve değerlendirmeyi yeniden deneyin.

## <a name="enter-commands"></a>Komutları girin

Büyüktür (>), Visual Studio komutları verirken oturum girin **hemen** penceresi. Kullanım **yukarı ok** ve **aşağı ok** anahtarlarını önceden kaydırmak için verilen komutları.

|Görev|Çözüm|Örnek|
|----------|--------------|-------------|
|İfadeyi değerlendirir.|İfade bir soru işareti (?) ile başlayın.|`? a+b`|
|Komut modu (tek bir komut çalıştırmak için) anlık modundayken geçici olarak girin.|Bunu koyarak komutu girin büyüktür işareti (>).|`>alias`|
|Komut penceresine geçiş yapın.|Girin `cmd` pencereye, önüne büyüktür işareti (>).|`>cmd`|
|Hemen penceresine geçin.|Girin `immed` pencereye büyüktür işareti (>) olmadan.|`immed`|

## <a name="mark-mode"></a>İşaret modu

İçinde herhangi bir önceki satırdaki tıkladığınızda **hemen** penceresinde tıklattığınızda, otomatik olarak işaretleme moduna. Bu, seçin, düzenleme ve herhangi bir metin düzenleyicisinde yaptığınız ve bunları geçerli satıra yapıştırmanıza gibi önceki komutların metnini kopyalamak sağlar.

## <a name="the-equals-sign-"></a>Eşittir işareti (=)

Girmek için kullanılan pencere `EvaluateStatement` komut belirleyen bir eşittir işareti (=) karşılaştırma işleci veya bir atama işleci olarak yorumlanır.

İçinde **hemen** penceresinde, eşittir işareti (=) bir atama işleci yorumlanır. Bunu, örneğin, komut

```cmd
>Debug.EvaluateStatement(varA=varB)
```

değişkenin değerini atar `varB` değişkene `varA`.

İçinde **komut** penceresinde, aksine, eşittir işareti (=) karşılaştırma işleci yorumlanır. Atama işlemlerini kullanamazsınız **komut** penceresi. Örneğin, bu nedenle, değişkenlerin değerleri `varA` ve `varB` farklı, sonra komutu

```cmd
>Debug.EvaluateStatement(varA=varB)
```

değerini döndürür `False`.

## <a name="first-chance-exception-notifications"></a>İlk fırsat özel durum bildirimleri

Bazı ayar yapılandırmalarında, ilk şans özel durum bildirimleri içinde görüntülenen **hemen** penceresi.

### <a name="toggle-first-chance-exception-notifications-in-the-immediate-window"></a>Hemen penceresinde geçiş ilk fırsat özel durum bildirimleri

1. Üzerinde **görünümü** menüsünde tıklatın **diğer Windows**, tıklatıp **çıkış**.

2. Metin alanına sağ **çıkış** penceresinde ve sonra seçin veya seçimini **özel durum iletileri**.

## <a name="see-also"></a>Ayrıca bkz.

- [Hata Ayıklayıcısı ile Kodlarda gezinme](../../debugger/navigating-through-code-with-the-debugger.md)
- [Komut Penceresi](../../ide/reference/command-window.md)
- [Hata ayıklayıcıya ilk bakış](../../debugger/debugger-feature-tour.md)
- [İzlenecek yol: Tasarım Zamanında Düzenleme](../../debugger/walkthrough-debugging-at-design-time.md)
- [Visual Studio Komut Diğer Adları](../../ide/reference/visual-studio-command-aliases.md)
- [Visual Studio'da Normal İfadeler Kullanma](../../ide/using-regular-expressions-in-visual-studio.md)
