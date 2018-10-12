---
title: Visual Studio için modelleme SDK'sı için API Başvurusu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 590c9a69-4e22-4841-bb23-f32e80ec1e76
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 7cb71263ec8c375ce7263b0b0ebf393cccde99be
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49211581"
---
# <a name="api-reference-for-modeling-sdk-for-visual-studio"></a>Visual Studio için Modelleme SDK'sı için API Başvurusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio Görselleştirme ve modelleme SDK'sı, etki alanına özgü diller (DSL) ve UML araçları oluşturulmuş bir platform sağlar.  
  
> [!NOTE]
>  UML modelleme API hakkında daha fazla bilgi için bkz. [UML modelleme genişletilebilirliği için API Başvurusu](../modeling/api-reference-for-uml-modeling-extensibility.md). Metin dönüştürme hakkında daha fazla bilgi için bkz. [T4 metin dönüştürmeyi özelleştirme](../modeling/customizing-t4-text-transformation.md).  
  
 Bu bölüm, adları "Microsoft.VisualStudio.Modeling" ile başlayan ad alanları için başvuru bilgileri içerir.  
  
|Ad Alanı|İçerik|  
|---------------|-------------|  
|<xref:Microsoft.VisualStudio.Modeling?displayProperty=fullName>|Bir DSL içinde tanımladığınız tüm etki alanı sınıflarının temel sınıf ModelElement gibi sınıflar.|  
|<xref:Microsoft.VisualStudio.Modeling.Design?displayProperty=fullName>|Bir DSL tanımının bir parçası form sınıflar.|  
|<xref:Microsoft.VisualStudio.Modeling.Diagnostics?displayProperty=fullName>|Model Store Görüntüleyicisi ve performans ölçümü araçlar.|  
|<xref:Microsoft.VisualStudio.Modeling.Diagrams?displayProperty=fullName>|Bir DSL içinde tanımladığınız tüm şekiller temel sınıfı olan ShapeElement gibi sınıflar.|  
|<xref:Microsoft.VisualStudio.Modeling.Diagrams.ExtensionEnablement?displayProperty=fullName>|Hareket ve seçim yöntemleri.|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition?displayProperty=fullName>|DSL tanımını Tasarımcı API'si.|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition.Design?displayProperty=fullName>|İç sınıflar DSL tanımını tasarımcının.|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition.ExtensionEnablement?displayProperty=fullName>|DSL Tasarımcısı komutlar ve hareketler doğrulama ile genişletmenizi sağlayan öznitelikler.|  
|<xref:Microsoft.VisualStudio.Modeling.Extensibility?displayProperty=fullName>|DSL genişletilebilirlik uygulamak ModelElement için genişletme yöntemleri.|  
|<xref:Microsoft.VisualStudio.Modeling.ExtensionEnablement?displayProperty=fullName>|Genişletilebilirlik öznitelikleri|  
|<xref:Microsoft.VisualStudio.Modeling.Immutability?displayProperty=fullName>|Salt okunur bir modelin parçalarını yapmanızı sağlar.|  
|<xref:Microsoft.VisualStudio.Modeling.Integration?displayProperty=fullName>|Yardımcı olan Modelbus API farklı modelleri tümleştirin.|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Picker?displayProperty=fullName>|İletişim kutusu, kullanıcıların modelleri ve Modelbus başvuru oluşturmak için öğeleri sağlar.|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Picker.Hosting?displayProperty=fullName>|Seçici hizmeti.|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Shell?displayProperty=fullName>|Modelbus bağdaştırıcısı framework [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Shell.Picker?displayProperty=fullName>|Seçici iletişim kutusu, kullanıcıların modelleri Modelbus başvuru oluşturmak için öğeleri gidip olanak sağlar.|  
|<xref:Microsoft.VisualStudio.Modeling.Shell?displayProperty=fullName>|DSL'ler arasında arabirim ve [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].|  
|<xref:Microsoft.VisualStudio.Modeling.Shell.ExtensionEnablement?displayProperty=fullName>|(Bağlam) kısayol menü komutları tanımlamanızı sağlar.|  
|<xref:Microsoft.VisualStudio.Modeling.Validation?displayProperty=fullName>|Doğrulama kısıtlamaları tanımlama olanak tanır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UML Genişletilebilirlik Modellemesi için API Başvurusu](../modeling/api-reference-for-uml-modeling-extensibility.md)   
 [T4 Metin Dönüştürmeyi Özelleştirme](../modeling/customizing-t4-text-transformation.md)



