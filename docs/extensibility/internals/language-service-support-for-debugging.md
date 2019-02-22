---
title: Hata ayıklama için dil hizmeti desteği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugger, language support
- language services, debugging support
ms.assetid: 7a44067f-a410-4a6a-84d2-bda5184140bc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 18856d2f3a6359a3be019e4e97e63832e896c2a9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56604749"
---
# <a name="language-service-support-for-debugging"></a>Hata Ayıklama için Dil Hizmeti Desteği
Dil hizmeti aracılığıyla bir hata ayıklayıcı desteği özellikleri sağlayabilir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageDebugInfo> arabirimi. Bu özellikler kesme noktalarını doğrulama ve ifadeleri listesini sağladığı **Otolar** penceresi.

 Ancak, bir ifade değerlendiricisi dilinizi hata ayıklamak için sahip olması. İfade değerlendirici, hata ayıklama sırasında değerler üretmek için ifadeleri değerlendirme için sorumludur. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz:

-   [CLR ifade değerlendiricisi](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators)

-   [Yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample)

## <a name="compiler-output"></a>Derleyici çıkışı
 Diliniz için hata ayıklama uygulamak için yapılması gerekenler derleyici türünü belirler. Derleyici, Windows işletim sistemini hedefleyen ve bir .pdb dosyası yazar, yerel kod hata ayıklama Visual Studio'ya entegre altyapısı ile programlar ayıklayabilirsiniz. Derleyicinizin Microsoft Ara dilini (MSIL) oluşturursa, Visual Studio ile de tümleştirilen altyapısı, hata ayıklama yönetilen kod ile programlar ayıklayabilirsiniz. Derleyici özel bir işletim sistemi veya farklı bir çalışma zamanı ortamı hedefliyorsa, kendi hata ayıklama motoru yazmanız gerekir.

 Diliniz için hata ayıklama uygulama konusunda daha fazla bilgi için bkz. [Başlarken](../../extensibility/debugger/getting-started-with-debugger-extensibility.md) hata ayıklama Visual Studio SDK.