---
title: Modelleme SDK'sı için API Başvurusu
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
ms.assetid: 590c9a69-4e22-4841-bb23-f32e80ec1e76
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6a290227b120958b5bb3407393dcff33b247b20d
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68872017"
---
# <a name="api-reference-for-modeling-sdk-for-visual-studio"></a>Visual Studio için Modelleme SDK'sı için API Başvurusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio Görselleştirme ve modelleme SDK'sı, etki alanına özgü diller (DSL) ve UML araçları oluşturulmuş bir platform sağlar.

> [!NOTE]
> UML modelleme API hakkında daha fazla bilgi için bkz. [UML modelleme genişletilebilirliği için API Başvurusu](../modeling/api-reference-for-uml-modeling-extensibility.md). Metin dönüştürme hakkında daha fazla bilgi için bkz. [T4 metin dönüştürmeyi özelleştirme](../modeling/customizing-t4-text-transformation.md).

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
|[Microsoft. VisualStudio. modelle tümleştirme](/previous-versions/ee904412(v=vs.140))|Yardımcı olan Modelbus API farklı modelleri tümleştirin.|
|[Microsoft. VisualStudio. modelle Integration. Picker](/previous-versions/ee904394(v=vs.140))|İletişim kutusu, kullanıcıların modelleri ve Modelbus başvuru oluşturmak için öğeleri sağlar.|
|`Microsoft.VisualStudio.Modeling.Integration.Picker.Hosting`|Seçici hizmeti.|
|[Microsoft. VisualStudio. modelle Integration. Shell](/previous-versions/ee869435(v=vs.140))|Modelbus bağdaştırıcısı framework [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].|
|[Microsoft. VisualStudio. modelle Integration. Shell. Picker](/previous-versions/ee886769(v=vs.140))|Seçici iletişim kutusu, kullanıcıların modelleri Modelbus başvuru oluşturmak için öğeleri gidip olanak sağlar.|
|<xref:Microsoft.VisualStudio.Modeling.Shell?displayProperty=fullName>|DSL'ler arasında arabirim ve [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].|
|<xref:Microsoft.VisualStudio.Modeling.Shell.ExtensionEnablement?displayProperty=fullName>|(Bağlam) kısayol menü komutları tanımlamanızı sağlar.|
|<xref:Microsoft.VisualStudio.Modeling.Validation?displayProperty=fullName>|Doğrulama kısıtlamaları tanımlama olanak tanır.|

## <a name="see-also"></a>Ayrıca bkz.

- [UML Genişletilebilirlik Modellemesi için API Başvurusu](../modeling/api-reference-for-uml-modeling-extensibility.md)
- [T4 Metin Dönüştürmeyi Özelleştirme](../modeling/customizing-t4-text-transformation.md)
