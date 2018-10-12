---
title: Hata ayıklama için dil hizmeti desteği | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugger, language support
- language services, debugging support
ms.assetid: 7a44067f-a410-4a6a-84d2-bda5184140bc
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a568ef30a26ad198d839ddcde257fec3036cf3c5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49173712"
---
# <a name="language-service-support-for-debugging"></a>Hata Ayıklama için Dil Hizmeti Desteği
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Dil hizmeti aracılığıyla bir hata ayıklayıcı desteği özellikleri sağlayabilir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageDebugInfo> arabirimi. Bu özellikler kesme noktalarını doğrulama ve ifadeleri listesini sağladığı **Otolar** penceresi.  
  
 Ancak, bir ifade değerlendiricisi dilinizi hata ayıklamak için sahip olması. İfade değerlendirici, hata ayıklama sırasında değerler üretmek için ifadeleri değerlendirme için sorumludur. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz:  
  
-   [CLR ifade değerlendiricisi](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators)  
  
-   [Yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample)  
  
## <a name="compiler-output"></a>Derleyici çıkışı  
 Diliniz için hata ayıklama uygulamak için yapılması gerekenler derleyici türünü belirler. Derleyici, Windows işletim sistemini hedefleyen ve bir .pdb dosyası yazar, yerel kod hata ayıklama Visual Studio'ya entegre altyapısı ile programlar ayıklayabilirsiniz. Derleyicinizin Microsoft Ara dilini (MSIL) oluşturursa, Visual Studio ile de tümleştirilen altyapısı, hata ayıklama yönetilen kod ile programlar ayıklayabilirsiniz. Derleyici özel bir işletim sistemi veya farklı bir çalışma zamanı ortamı hedefliyorsa, kendi hata ayıklama motoru yazmanız gerekir.  
  
 Diliniz için hata ayıklama uygulama konusunda daha fazla bilgi için bkz. [Başlarken](../../extensibility/debugger/getting-started-with-debugger-extensibility.md) hata ayıklama Visual Studio SDK.

