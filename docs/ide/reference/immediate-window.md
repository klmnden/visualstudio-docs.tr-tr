---
title: Komut Penceresi
ms.date: 02/25/2019
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
ms.openlocfilehash: e3a8315b087e259e7e1e37dfa8ab30d476bea308
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/27/2019
ms.locfileid: "56954205"
---
# <a name="immediate-window"></a>Komut penceresi

Kullanım **hemen** penceresi hata ayıklama ve ifade değerlendirme, deyimleri yürütmek ve değişken değerlerini yazdırma. **Hemen** penceresi oluşturma ve şu anda seçili proje kullanarak ifadeleri değerlendirir.

Görüntülenecek **hemen** penceresinde düzenlemeye yönelik bir proje açın ve ardından **hata ayıklama** > **Windows** > **hemen**  veya basın **Ctrl**+**Alt**+**miyim**. Ayrıca girebilirsiniz **Debug.Immediate** içinde **komut** penceresi.

**Hemen** penceresi de IntelliSense'i destekler.

## <a name="display-the-values-of-variables"></a>Değişkenlerin değerlerini görüntüleme

**Hemen** uygulama hata ayıklama işlemi yaparken penceresi özellikle yararlıdır. Örneğin, bir değişkenin değerini denetlemek için `varA`, kullanabileceğiniz [yazdırma komut](../../ide/reference/print-command.md):

```cmd
>Debug.Print varA
```

Soru işareti (?) için bir diğer addır `Debug.Print`, bu komut ayrıca yazılabilir:

```cmd
? varA
```

Bu komutun her iki sürümü değişken değerini döndürmek `varA`.

> [!TIP]
> Bir Visual Studio komut vermek için **hemen** penceresinde komutun önüne gerekir büyüktür işareti (>). Birden fazla komut girmek için geçin [komut penceresi](command-window.md).

## <a name="design-time-expression-evaluation"></a>Tasarım zamanı ifade değerlendirmesi

Kullanabileceğiniz **hemen** tasarım zamanında bir işlev veya alt yordamı yürütmek için pencere.

### <a name="execute-a-function-at-design-time"></a>Tasarım zamanında bir işlevi yürütmek

1. Aşağıdaki kod, bir Visual Basic konsol uygulamasına kopyalayın:

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

2. Üzerinde **hata ayıklama** menüsünde seçin **Windows** > **hemen**.

3. Tür `?MyFunction(2)` içinde **hemen** penceresi ve ENTER tuşuna **Enter**.

    **Hemen** penceresi çalıştıran `MyFunction` ve görüntüler `4`.

Visual Studio, işlev veya alt yordam bir kesme noktası içeriyorsa, uygun noktada yürütmeyi keser. Ardından, programınızın durumunu incelemek için hata ayıklayıcı penceresini kullanabilirsiniz. Daha fazla bilgi için [izlenecek yol: Tasarım zamanında hata ayıklama](../../debugger/walkthrough-debugging-at-design-time.md).

Office projeleri, web projeleri, akıllı cihaz projeleri ve SQL projeleri için Visual Studio Araçları da dahil olmak üzere bir yürütme ortamı gerektiren proje türlerinde tasarım zamanı ifade değerlendirmesini kullanamazsınız.

### <a name="design-time-expression-evaluation-in-multi-project-solutions"></a>Çoklu proje çözümlerinde tasarım zamanı ifade değerlendirmesi

Tasarım zamanı ifade değerlendirme bağlamının sağlarken, Visual Studio Çözüm Gezgini'nde seçili olan projeye başvurur. Çözüm Gezgini'nde proje seçtiyseniz, Visual Studio Başlangıç projesine karşı işlevi değerlendirmeye çalışır. İşlev geçerli bağlamda değerlendirilemezse, bir hata iletisi alırsınız. Çözümün başlangıç projesi olmayan bir projede bir işlevi değerlendirilemiyor çalıştığınız ve bir hata alırsanız, Çözüm Gezgini'nde projeyi seçmeyi deneyin ve değerlendirmeyi yeniden deneyin.

## <a name="enter-commands"></a>Komutları girin

Büyüktür (>), Visual Studio komutları verirken oturum girin **hemen** penceresi. Kullanım **yukarı ok** ve **aşağı ok** , önceden kullanılmış komutlarda gezinmek için anahtarları.

|Görev|Çözüm|Örnek|
|----------|--------------|-------------|
|İfadeyi değerlendirir.|İfade bir soru işareti (?) ile başlayın.|`? a+b`|
|Komut modu (tek bir komut çalıştırmak için) anlık modundayken geçici olarak girin.|Bunu koyarak komutu girin büyüktür işareti (>).|`>alias`|
|Komut penceresine geçiş yapın.|Girin `cmd` pencereye, önüne büyüktür işareti (>).|`>cmd`|
|Hemen penceresine geçin.|Girin `immed` pencereye büyüktür işareti (>) olmadan.|`immed`|

## <a name="mark-mode"></a>İşaret modu

İçinde herhangi bir önceki satırdaki tıkladığınızda **hemen** penceresinde tıklattığınızda, otomatik olarak işaretleme moduna. Bu, seçin, düzenleme ve herhangi bir metin düzenleyicisinde yaptığınız ve bunları geçerli satıra yapıştırmanıza gibi önceki komutların metnini kopyalamak sağlar.

## <a name="examples"></a>Örnekler

Aşağıdaki örnek, dört ifadeleri ve bunların sonucunda gösterir **hemen** penceresi Visual Basic projesi için.

```cmd
j = 2
Expression has been evaluated and has no value

? j
2

j = DateTime.Now.Day
Expression has been evaluated and has no value

? j
26
```

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
