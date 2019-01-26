---
title: Sembol sağlayıcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- symbol handler
- debugging [Debugging SDK], symbol handler
ms.assetid: 5fce651b-fead-4418-81b0-a011df7644ab
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed25959cd6afa7232555757e358a99836d93924b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54981486"
---
# <a name="symbol-provider"></a>Sembol sağlayıcısı
Bir ifade değerlendiricisi uygulama değişkenleri ve ifadeleri değerlendirilebilmesi için dil derleyicisi tarafından üretilen sembolik hata ayıklama bilgileri erişmeniz gerekir. Bunu bir sembol işleyici olarak da adlandırılan bir sembol sağlayıcısı (SP) arabirimleri kullanma tarafından yapar.  
  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Program veritabanı (PDB) sembolü dosya biçimi kullanılarak yerel kod yanı sıra yönetilen kod için SPs sağlar. Olmadığı sürece güçlü özel biçiminde depolanan semboller kullanmak, programınız için gerekir, bu tarafından sağlanan SPs kullanmanız önerilir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
## <a name="implementation-notes"></a>Uygulama notları  
 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Hata ayıklama motorlarını beklediğiniz ortak dil çalışma zamanı (CLR) arabirimlerini kullanarak SPs ile bahsedeceğiz. Sonuç olarak, Visual Studio hata ayıklama altyapıları ile çalışan bir SP CLR desteklemesi gerekir. Hata ayıklama arabirimleri tüm CLR tam listesi parçası olan debugref.doc içinde bulunabilir, [!INCLUDE[winsdklong](../../deployment/includes/winsdklong_md.md)].  
  
 Yalnızca özel hata ayıklama altyapısıyla, SP çalışacaksınız ise, hata ayıklama altyapısı gereksinimlerine bağlı olarak uygun gördüğünüz şekilde SP uygulayabilirsiniz.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)