---
title: Kesme noktası isabet iletişim kutusu olduğunda | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.whenbreakpointishit
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
ms.assetid: 476e3d98-cf35-4338-b124-cd0f3010d854
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d4cc3c2366ca20328f591b0661e8c2b3e5af1e45
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56717708"
---
# <a name="when-breakpoint-is-hit-dialog-box"></a>Kesme Noktası İsabet Edildiğinde İletişim Kutusu
Bu iletişim kutusu ile bir kesme noktasına gelindiğinde gerçekleşen eylemi özelleştirebilirsiniz.

## <a name="uielement-list"></a>UIElement Listesi
 **İleti Yazdır** DebuggerDisplay sözdizimini kullanarak, bir ileti yazdırır. Daha fazla bilgi için [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md).

 Bu metin kutusu, bir DebuggerDisplay ifadesinin küme ayraçları içinde veya tek başlarına kullanılabilecek özel anahtar sözcükleri (örneğin, $ADDRESS) de destekler. Kullanılabilir anahtar sözcükler, iletişim kutusunda listelenir.

 **Yürütmeye devam et** bu denetimin etkin olup yalnızca **ileti Yazdır** seçilir. Bu denetim seçildiğinde, bir kesme noktasını, konuma ulaşıldığında kesmek yerine, program yürütmenizi izlemek üzere bir izleme noktası olarak kullanabilirsiniz.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kesme Noktalarını Kullanma](../debugger/using-breakpoints.md)
- [DebuggerDisplay Özniteliğini Kullanma](../debugger/using-the-debuggerdisplay-attribute.md)