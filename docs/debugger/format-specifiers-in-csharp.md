---
title: Biçim belirleyiciler hata ayıklayıcı (C#) | Microsoft Docs
ms.date: 11/21/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- expressions [C#], formatting values
- variables [debugger], watch variable symbols
- symbols, watch variable formatting
- QuickWatch dialog box, using format specifiers
- specifiers, watch variable format
- QuickWatch dialog box, format specifiers in C#
- specifiers
- watch variable symbols
- Watch window, format specifiers in C#
- format specifiers, debugger
- debugger, format specifiers recognized by
ms.assetid: 345c8589-5f36-4d34-a58c-e56271687dd6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: caaf36e286f1bdc664ebdbb10e3baf7ed28183e7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62849829"
---
# <a name="format-specifiers-in-c-in-the-visual-studio-debugger"></a>Biçim belirleyiciler içinde C# Visual Studio hata ayıklayıcısı
İçinde bir değer görüntülenir biçimini değiştirebilirsiniz **Watch** biçim belirticilerini kullanarak pencere. İçindeki Biçim belirticileri kullanabilirsiniz **hemen** penceresinde **komut** penceresi, [izleme noktaları](../debugger/using-breakpoints.md#BKMK_Print_to_the_Output_window_with_tracepoints)ve kaynak pencerelerinde. Bu pencereler içinde bir ifade üzerinde duraklarsanız, sonuç görünür bir [DataTip](../debugger/view-data-values-in-data-tips-in-the-code-editor.md) belirtilen biçim görüntülenir.

Bir biçim belirtici kullanmak için bir virgül ve uygun belirticisi tarafından değişken ifade girin.

## <a name="set-format-specifiers"></a>Biçim belirticileri kümesi
Aşağıdaki kod örneği kullanacağız:

```csharp
{
    int my_var1 = 0x0065;
    int my_var2 = 0x0066;
    int my_var3 = 0x0067;
}
```

Ekleme `my_var1` değişkenini **Watch** hata ayıklarken, pencere **hata ayıklama** > **Windows** > **izleyin**  >  **1 izleyin**. Ardından, değişkeni sağ tıklatın ve seçin **onaltılık gösterim**. Artık **Watch** penceresi 0x0065 değeri gösterir. Bu değer bir onaltılık tamsayı yerine bir ondalık tamsayı olarak görmek için ondalık biçim belirteci ekleme **, d** içinde **adı** değişken adından sonra sütun. **Değer** sütun gösterdiğini **101**.

![WatchFormatCSharp](../debugger/media/watchformatcsharp.png "WatchFormatCSharp")

::: moniker range=">= vs-2019" 

Görüntüleyebilir ve değeri bir virgül (,) ekleyerek kullanılabilir biçim belirleyicilerinin bir listeden seçim **Watch** penceresi. 

![FormatSpecCSharp](../debugger/media/vs-2019/format-specs-csharp.png "FormatSpecCSharp")

::: moniker-end

## <a name="format-specifiers"></a>Biçim belirticileri
Aşağıdaki tabloda açıklanmıştır C# biçim belirleyiciler Visual Studio hata ayıklayıcı için.

|Belirleyici|Biçimi|Özgün izleme değeri|Görüntüler|
|---------------|------------|--------------------------|--------------|
|AC|Örtülü değerlendirme özellikleri ve örtük işlev çağrılarını devre dışı bırakıldığında, yararlı olabilecek bir ifade değerlendirmesi zorlar.|"Kapalı işlev değerlendirme kullanıcı tarafından devre dışı" iletisi|\<Değer >|
|d|Ondalık tamsayı|0x0065|101|
|dinamik|Dinamik bir görünümü kullanarak belirtilen nesneyi görüntüler|Dinamik görünüm dahil olmak üzere nesnenin tüm üyelerini görüntüler|Yalnızca dinamik görünüm görüntüler|
|h|Onaltılık tamsayı|61541|0x0000F065|
|Nq|hiçbir tırnak işaretleri dize|"Benim dize"|My dize|
|nse|Davranış biçimini değil belirtir. "Yan etkiler" ifadesiyle değerlendirir. İfade yorumlanamıyor ve yalnızca Değerlendirme sürümü (örneğin, bir işlev çağrısı) çözülebilir, bunun yerine bir hata görürsünüz.|Yok|Yok|
|gizli|Tüm genel ve genel olmayan üyeleri görüntüler|Görüntüler Genel üyeler|Tüm üyelerini görüntüler|
|Ham|Ham madde düğümüne göründüğü gibi öğesi görüntüler. Proxy nesneleri yalnızca geçerli.|Sözlük\<T >|Sözlük işlenmemiş bir görünümünü\<T >|
|sonuçlar|IEnumerable veya IEnumerable uygulayan bir tür değişkeninin ile kullanılan\<T >, genellikle bir sorgu ifadesinin sonucu. Sorgu sonucu içeren üyelerini görüntüler.|Tüm üyelerini görüntüler|Üyeleri karşılamak görüntüler sorgunun koşulları|

## <a name="see-also"></a>Ayrıca bkz.
- [İzleme ve QuickWatch windows](../debugger/watch-and-quickwatch-windows.md)
- [Otolar ve yerel öğeler pencerelerinde](../debugger/autos-and-locals-windows.md)
