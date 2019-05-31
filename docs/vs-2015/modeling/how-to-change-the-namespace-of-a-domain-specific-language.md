---
title: 'Nasıl yapılır: Bir etki alanına özgü dil Namespace Değiştir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, namespace
ms.assetid: f20c47e5-230d-4f0e-812f-5c6edb86866c
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e86fa8f220cdd31beae12e050a1cbaa592624a74
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65690563"
---
# <a name="how-to-change-the-namespace-of-a-domain-specific-language"></a>Nasıl yapılır: Alana Özgü bir Dilin Ad Alanını Değiştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Etki alanına özgü bir dilin ad alanını değiştirebilirsiniz. Değişiklik yapmanız gereken **DSL Gezgini**, Dsl paket proje özelliklerinde ve derleme bilgileri.  
  
### <a name="to-change-the-namespace-of-a-domain-specific-language"></a>Etki alanına özgü bir dilin ad alanını değiştirmek için  
  
1. İçinde **DSL Gezgini**, tıklayın **Dsl** düğümü.  
  
2. İçinde **özellikleri** penceresinde değişiklik **Namespace** özelliği.  
  
3. Çözüm kaydedin ve şablonlarını Dönüştür.  
  
4. Üzerinde **proje** menüsünü tıklatın **Dsl özellikleri**.  
  
     Projeniz için Özellikler görünür.  
  
5. Tıklayın **uygulama** sekmesi.  
  
6. Değişiklik **varsayılan ad alanı** özelliğini yeni ad alanı adı.  
  
7. Derlemenin adı değiştirmek istiyorsanız, değişiklik **bütünleştirilmiş kodun ad özelliği.**  
  
8. Derleme adı değişmişse DslPackage\Package.tt açın ve bu satırı güncelleştirin:  
  
     `string dslAssembly = "YourDSLassembly.Dsl.dll";`  
  
9. Herhangi bir özel kod yazdığınız, kod dosyalarında ad alanını ve sınıf başvuruları değiştirdiğinizden emin olun.  
  
10. Visual Studio deneysel örneği sıfırlayın.  
  
    1. Silme **\Users\\** _{adınız}_ **\AppData\Local\Microsoft\VisualStudio\\\*üs**  
  
    2. Windows üzerinde **Başlat** menüsünde seçin **tüm programlar**, **Microsoft Visual Studio 2010 SDK**, **Araçları**, **Sıfırla Deneysel örneği**.  
  
11. Üzerinde **derleme** menüsünde seçin **çözümü yeniden derle**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
