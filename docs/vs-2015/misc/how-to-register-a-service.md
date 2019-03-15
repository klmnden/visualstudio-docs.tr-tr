---
title: 'Nasıl yapılır: Bir hizmet kaydı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- services, registering
ms.assetid: d086be78-ec3c-43cc-b799-5180a71e19f1
caps.latest.revision: 16
manager: jillfra
ms.openlocfilehash: 0ec69fa123775cb477195d4022fb439fb990f415
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57872854"
---
# <a name="how-to-register-a-service"></a>Nasıl yapılır: Bir hizmeti kaydedin
Yönetilen paket çerçevesini (MPF), yönetilen hizmetler kaydını denetlemek için öznitelikleri sağlar. RegPkg yardımcı programı bir hizmetiyle kaydetmek için bu öznitelikler kullanan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod dandır [VSSDK örnekleri](../misc/vssdk-samples.md).  
  
 [!code-csharp[VSSDKRegisterService#1](../snippets/csharp/VS_Snippets_VSSDK/vssdkregisterservice/cs/vssdkregisterservicepackage.cs#1)]
 [!code-vb[VSSDKRegisterService#1](../snippets/visualbasic/VS_Snippets_VSSDK/vssdkregisterservice/vb/vssdkregisterservicepackage.vb#1)]  
  
 <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute> SMyGlobalService hizmetine kaydeder [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.Shell.DefaultRegistryRootAttribute> ve <xref:Microsoft.VisualStudio.Shell.PackageRegistrationAttribute>, bkz: [kaydetme ve kaydını kaldırma VSPackages](../extensibility/registering-and-unregistering-vspackages.md).  
  
 Aynı ada sahip başka bir hizmete yerini alan bir hizmeti kaydetmek için kullanın <xref:Microsoft.VisualStudio.Shell.ProvideServiceOverrideAttribute> yerine <xref:Microsoft.VisualStudio.Shell.ProvideServiceAttribute>.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 Bir hizmet sağlayıcısı hizmeti istemcisi değiştirmeden yeniden derleyin daha kolay hale getirmek için veya tam tersi hizmet ve arabirimlerini ayrı derleme modülünde tanımlayabilirsiniz. Aşağıdaki kod Reference.Services (C#) örnek IMyGlobalService.cs dosyasında arasındadır.  
  
 [!code-csharp[VSSDKRegisterService#2](../snippets/csharp/VS_Snippets_VSSDK/vssdkregisterservice/cs/vssdkregisterservicepackage.cs#2)]
 [!code-vb[VSSDKRegisterService#2](../snippets/visualbasic/VS_Snippets_VSSDK/vssdkregisterservice/vb/vssdkregisterservicepackage.vb#2)]  
  
 <xref:System.Runtime.InteropServices.ComVisibleAttribute> Arabirimi, yönetilmeyen koddan elde etmek için gereklidir.  
  
> [!NOTE]
>  Hizmet ve arabirimi için aynı türe veya GUID kullanabilirsiniz, ancak bir hizmet farklı arabirimleri kullanıma sunabileceğinden iki ayrı öneririz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackage'ları kaydetme](../extensibility/internals/registering-vspackages.md)   
 [Hizmet Temel Bileşenleri](../extensibility/internals/service-essentials.md)