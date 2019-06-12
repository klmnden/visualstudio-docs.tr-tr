---
title: 'SharePoint çözümleri: Özel özellik oluştur, paket doğrulama kuralları'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, extending deployment
- SharePoint development in Visual Studio, validation rules
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a10118a0c83f9e17e32efd293a9a824e38a0942a
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66835933"
---
# <a name="how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions"></a>Nasıl yapılır: Özel özellik ve paket doğrulama kuralları için SharePoint çözümleri oluşturma
  Visual Studio tarafından oluşturulan çözüm paketi doğrulamak için özel doğrulama kuralları oluşturabilirsiniz. Seçerek bir özelliğin tamamı veya paketin tam doğrulama gerçekleştirebilirsiniz **doğrulama** bir paket veya özelliği, bağlam menüsünden **PackagingExplorer**. Özellik ve paket geçerli bir durumda olmaya istekli olup olmadığını belirlemek için projeye yeni özellik veya SharePoint Proje öğeleri eklediğinizde, kısmi doğrulama gerçekleştirilir.

### <a name="to-create-a-custom-package-validation-rule"></a>Özel paket doğrulama kuralı oluşturmak için

1. Bir sınıf kitaplığı projesi oluşturun.

2. Aşağıdaki derlemelere başvurular ekleyin:

    - Microsoft.VisualStudio.SharePoint

    - System.ComponentModel.Composition

3. Aşağıdaki arabirimlerinden birini uygulayan bir sınıf oluşturun:

    - Paket doğrulama kuralı oluşturmak için uygulaması <xref:Microsoft.VisualStudio.SharePoint.Validation.IPackageValidationRule> arabirimi.

    - Bir özellik doğrulama kuralı oluşturmak için uygulaması <xref:Microsoft.VisualStudio.SharePoint.Validation.IFeatureValidationRule> arabirimi.

4. Ekleme <xref:System.ComponentModel.Composition.ExportAttribute> sınıfa. Bu öznitelik, bulma ve doğrulama kuralınızı yüklemek Visual Studio sağlar. Geçirmek <xref:Microsoft.VisualStudio.SharePoint.Validation.IPackageValidationRule> veya <xref:Microsoft.VisualStudio.SharePoint.Validation.IFeatureValidationRule> özniteliği Oluşturucu türü.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir özel özellik doğrulama kuralının nasıl oluşturulacağını gösterir.

 [!code-vb[SPExtensibility.FeatureValidation#1](../sharepoint/codesnippet/VisualBasic/featurevalidation/extension/customvalidationrule.vb#1)]
 [!code-csharp[SPExtensibility.FeatureValidation#1](../sharepoint/codesnippet/CSharp/featurevalidation/extension/customfeaturevalidationrule.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

- Microsoft.VisualStudio.SharePoint.

- System.ComponentModel.Composition.

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [uzantıları dağıtmak için SharePoint araçları Visual Studio'da](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)
