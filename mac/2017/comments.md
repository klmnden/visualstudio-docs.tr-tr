---
title: Kodu açıklama
description: Bu makalede, Mac için Visual Studio kaynak düzenleyicisinde açıklamalar kullanılarak açıklanır.
author: conceptdev
ms.author: crdun
ms.date: 05/06/2018
ms.assetid: 0FE5E929-1846-4F48-B5E3-70990FAF9504
ms.openlocfilehash: 1f792e5ba670854e4a3a9ce703212d18c16e5512
ms.sourcegitcommit: da73f7a0cf1795d5d400c0897ae3326191435dd0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/28/2019
ms.locfileid: "58573086"
---
# <a name="comments"></a>Açıklamalar

Hata ayıklama veya kodla denemeler, kod bloklarını ya da geçici olarak açıklama satırı yapın veya uzun süreli yararlı olabilir.

Tüm bir kod bloğunu açıklama eklemek için:

* Kod seçip **geçiş _Satır** bağlam menüsünden

VEYA

* Kullanım `cmd + /` tuş üzerinde seçili kod.

Bu yöntemler, açıklama ve kodun bölümlerine için kullanılabilir. C# dosyaları ek düzeyleri satırlı yorumlar, açıklanmış ve açıklamalı olmayan çalışırken yine de koruma gerçek yorumları kodlarının bölgeleri sağlayan eklenebilir:

![çok düzeyli açıklamaları](media/source-editor-image8.png)

Açıklamalar, panoyla etkileşim gelecekteki geliştiriciler için kod belgeleme için kullanışlıdır. Bunlar genellikle şu şekilde her dilde eklenen çok satırlı yorumlar biçiminde gerçekleştirilir:

**C#**

```csharp
/*
 This is a multi-line
 comment in C#
*/
```

**F#**

```fsharp
(*
 This is a multi-line
  comment in F#
*)
```

## <a name="see-also"></a>Ayrıca bkz.

- [Kod (Windows için Visual Studio) açıklama satırı yapın](/visualstudio/ide/quickstart-editor#comment-out-code)