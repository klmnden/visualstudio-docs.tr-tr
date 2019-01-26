---
title: Yapılandırma ve SelectedItem nesneleri için Otomasyon | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], SelectedItem object
- automation [Visual Studio SDK], builds
ms.assetid: 120377f1-51aa-4445-b2f7-06ab7fc2b47f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 60efbb25b0b5b52e1392ce84c16710a78dde7b16
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54919284"
---
# <a name="automation-for-configuration-and-selecteditem-objects"></a>Yapılandırma ve SelectedItem nesneleri için Otomasyon
Derleme ve seçili öğe işlemlerini otomatik hale getirebilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].  
  
## <a name="automation-for-builds"></a>Yapılar için Otomasyon  
 Derleme veya yapılandırma, uyguladığınızda sağlanan bir otomasyon modeli olan <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider>. Daha fazla bilgi için [anlayın derleme yapılandırmaları](../../ide/understanding-build-configurations.md).  
  
 VSPackage'ı oluşturma ve yapılandırma seçeneklerini denetlemek isterseniz, otomasyon modeli kullanmanız gerekir.  
  
## <a name="automation-for-selecteditem"></a>SelectedItem için Otomasyon  
 Bir uygulama için sağlaması gerekmez `SelectedItem` Visual Studio standart uygulaması içerdiğinden nesne. Ancak, uygulayabileceğiniz `SelectedItem` tercih ederseniz nesne. İçeren bir nesne uygulamalıdır `SelectedItem` arabirim ve çağrısı için bir yanıt döndüreceğini <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> yöntemiyle `VSITEMID` kümesine <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID>.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A>   
 [Otomasyon modeline katkıda bulunma](../../extensibility/internals/contributing-to-the-automation-model.md)   
 [Derleme yapılandırmalarını anlama](../../ide/understanding-build-configurations.md)