---
title: Projeleri iç içe geçirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project nesting
- nested projects
- projects [Visual Studio SDK], child projects
- projects [Visual Studio SDK], nesting
ms.assetid: 12cce037-9840-4761-845e-5abd5fb317b0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2ee02bbe830c8ef3eab5766cd97a4c04837dc585
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55014026"
---
# <a name="nesting-projects"></a>Projeleri İç İçe Geçirme
VS paketinizi kullanan kurumsal uygulama geliştiriciler rahatça benzer türde bir araya projeleri grup [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kullanarak *iç içe proje*. Örneğin, kuruluş şablon proje grubu projeleri için iç içe projeler kategoriler halinde kullanır. İş cephe projeleri, Web kullanıcı arabirimini projeleri ve benzeri bir kategoriye birlikte gruplandırılır.  
  
 Bu senaryoda, sınır yoktur Geliştirici her üst projesi altında iç içe projeler sayısının Geliştirici program aracılığıyla sınırları sağlamasına karşın. Bu tür bir gruplandırma, yinelemeli, bu durumda alt, üst öğesinin bir alt proje niteliğindeki bir alt proje olmasını alt altında bir alt proje ile aynı türden projeleri yuvalanabilir de yapılabilir.  
  
 Proje iç içe geçme iç bir parçası değil [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. İç içe geçirmeyi etkinleştirin ve alt projeleri içinde iç içe alt proje için kod yazmak zorunda. Ana proje özel VSPackage'ı veya oluşturulan ve kaydettirilen proje iç içe geçirmeyi uygulamak için gereken kodu içeren kendi GUİD'li proje türü, ' dir.  
  
 C# Example.Nested proje örnekte iç içe projeler örneği bulabilirsiniz.  
  
## <a name="nested-projects-example"></a>İç içe projeler örneği  
 ![İç içe projeler çözüm](../../extensibility/internals/media/vsnestedprojects.gif "vsNestedProjects")  
İç içe projeler örneği  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: İç içe Projeler uygulama](../../extensibility/internals/how-to-implement-nested-projects.md)   
 [Kaldırma ve yeniden yükleme iç içe projeler için dikkat edilmesi gerekenler](../../extensibility/internals/considerations-for-unloading-and-reloading-nested-projects.md)   
 [İç içe projeler için sihirbaz desteği](../../extensibility/internals/wizard-support-for-nested-projects.md)   
 [Proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md)   
 [İç içe projeler için komut işlemesi uygulama](../../extensibility/internals/implementing-command-handling-for-nested-projects.md)   
 [İç içe projeler için addItem iletişim kutusunu filtreleme](../../extensibility/internals/filtering-the-additem-dialog-box-for-nested-projects.md)   
 [Denetim listesi: Yeni proje türleri oluşturma](../../extensibility/internals/checklist-creating-new-project-types.md)   
 [Bağlam parametreleri](../../extensibility/internals/context-parameters.md)   
 [Sihirbaz (.Vsz) Dosyası](../../extensibility/internals/wizard-dot-vsz-file.md)