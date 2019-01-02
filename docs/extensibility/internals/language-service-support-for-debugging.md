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
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 1963dad4861ad9026a683c695cf25a6becff7571
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53841364"
---
# <a name="language-service-support-for-debugging"></a>Hata Ayıklama için Dil Hizmeti Desteği
Dil hizmeti aracılığıyla bir hata ayıklayıcı desteği özellikleri sağlayabilir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageDebugInfo> arabirimi. Bu özellikler kesme noktalarını doğrulama ve ifadeleri listesini sağladığı **Otolar** penceresi.  
  
 Ancak, bir ifade değerlendiricisi dilinizi hata ayıklamak için sahip olması. İfade değerlendirici, hata ayıklama sırasında değerler üretmek için ifadeleri değerlendirme için sorumludur. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz:  
  
-   [CLR ifade değerlendiricisi](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators)  
  
-   [Yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample)  
  
## <a name="compiler-output"></a>Derleyici çıkışı  
 Diliniz için hata ayıklama uygulamak için yapılması gerekenler derleyici türünü belirler. Derleyici, Windows işletim sistemini hedefleyen ve bir .pdb dosyası yazar, yerel kod hata ayıklama Visual Studio'ya entegre altyapısı ile programlar ayıklayabilirsiniz. Derleyicinizin Microsoft Ara dilini (MSIL) oluşturursa, Visual Studio ile de tümleştirilen altyapısı, hata ayıklama yönetilen kod ile programlar ayıklayabilirsiniz. Derleyici özel bir işletim sistemi veya farklı bir çalışma zamanı ortamı hedefliyorsa, kendi hata ayıklama motoru yazmanız gerekir.  
  
 Diliniz için hata ayıklama uygulama konusunda daha fazla bilgi için bkz. [Başlarken](../../extensibility/debugger/getting-started-with-debugger-extensibility.md) hata ayıklama Visual Studio SDK.