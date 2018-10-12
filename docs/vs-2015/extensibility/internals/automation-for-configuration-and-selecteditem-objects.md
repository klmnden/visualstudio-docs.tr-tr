---
title: Yapılandırma ve SelectedItem nesneleri için Otomasyon | Microsoft Docs
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
- automation [Visual Studio SDK], SelectedItem object
- automation [Visual Studio SDK], builds
ms.assetid: 120377f1-51aa-4445-b2f7-06ab7fc2b47f
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 80c67567a3e9ed3fd482a9a88f6d52cddcc0a3e5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49185425"
---
# <a name="automation-for-configuration-and-selecteditem-objects"></a>Yapılandırma ve SelectedItem Nesneleri için Otomasyon
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Derleme ve seçili öğe işlemlerini otomatik hale getirebilirsiniz [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
## <a name="automation-for-builds"></a>Yapılar için Otomasyon  
 Derleme veya yapılandırma, uyguladığınızda sağlanan bir otomasyon modeli olan <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgProvider>. Daha fazla bilgi için [derleme yapılandırmalarını anlama](../../ide/understanding-build-configurations.md).  
  
 VSPackage'ı oluşturma ve yapılandırma seçeneklerini denetlemek isterseniz, otomasyon modeli kullanmanız gerekir.  
  
## <a name="automation-for-selecteditem"></a>SelectedItem için Otomasyon  
 Bir uygulama için sağlaması gerekmez `SelectedItem` Visual Studio standart uygulaması içerdiğinden nesne. Ancak, uygulayabileceğiniz `SelectedItem` tercih ederseniz nesne. İçeren bir nesne uygulamalıdır `SelectedItem` arabirim ve çağrısı için bir yanıt döndüreceğini <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A> VSITEMID yöntemiyle kümesine <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID>.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage%2A>   
 [Otomasyon modeline katkıda bulunma](../../extensibility/internals/contributing-to-the-automation-model.md)   
 [Derleme Yapılandırmalarını Anlama](../../ide/understanding-build-configurations.md)

