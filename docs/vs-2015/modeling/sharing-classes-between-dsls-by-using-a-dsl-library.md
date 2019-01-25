---
title: DSL kitaplığı kullanarak DSL'ler arasında sınıfları paylaşma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 509bd96b-3e66-47f4-8642-771421d0d0d5
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0c3a14a254eb3b07a95687faaf377664dd6f747a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54780882"
---
# <a name="sharing-classes-between-dsls-by-using-a-dsl-library"></a>DSL Kitaplığı Kullanarak DSL'ler Arasında Sınıfları Paylaşma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Görselleştirme ve modelleme SDK'si, başka bir DSL alabilir tamamlanmamış bir DSL tanımını oluşturabilirsiniz. Bu, benzer modeller ortak bölümlerini faktörü sağlar.  
  
## <a name="creating-and-using-dsl-libraries"></a>DSL kitaplığı kullanarak ve oluşturma  
  
#### <a name="to-create-a-dsl-library"></a>DSL kitaplığı oluşturmak için  
  
1.  Yeni bir DSL projesi oluşturun ve DSL kitaplığı çözüm şablonu seçin.  
  
     Tek bir DSL projesi ile boş bir model oluşturulur.  
  
2.  Etki alanı sınıfları, ilişkilerini, Şekil vb. ekleyebilirsiniz.  
  
     Kitaplık öğelerinde, tek bir gömme ağacı oluşturmak sahip değilsiniz.  
  
     Importers kullanabileceğiniz bir ilişki tanımlamak için iki alan sınıfı oluşturun ve bunlar arasında ilişki oluşturun.  
  
     Ayarlamayı düşünün **devralma değiştiricisi** için etki alanı sınıflarının `Abstract`.  
  
3.  DSL Gezgini bağlantı oluşturucular gibi tanımlayan öğeler ekleyebilirsiniz.  
  
4.  Doğrulama kısıtlamaları gibi ek kod gerektiren özelleştirmeler ekleyebilirsiniz.  
  
5.  Tıklayın **tüm şablonları dönüştürme**.  
  
6.  Projeyi oluşturun.  
  
7.  DSL kullanılacak diğer kişiler için dağıttığınızda, hem derlemede (DLL) hem de dosyanın sağlamalıdır `DslDefinition.dsl`. Derlenmiş bütünleştirilmiş kod klasörü altında bulabilirsiniz `Dsl\bin\*`  
  
#### <a name="to-import-a-dsl-library"></a>DSL kitaplığı içeri aktarmak için  
  
1. Başka bir DSL tanımındaki içinde **DSL Gezgini**DSL kök sınıfının sağ tıklayın ve ardından **ekleme yeni DslLibrary alma**.  
  
2. Özellikler penceresinde ayarlayın **dosya yolu** kitaplığı. Bir göreli veya mutlak bir yol kullanabilirsiniz.  
  
    İçeri aktarılan kitaplık salt okunur modda DSL Gezgini'nde görünür.  
  
3. İçeri aktarılan sınıflar temel sınıf olarak kullanabilirsiniz. İçeri aktarma DSL içinde alan sınıfı oluşturun ve Özellikler penceresinde ayarlayın **temel sınıf** içeri aktarılan bir sınıf.  
  
4. Tüm Şablonları Dönüştür tıklayın.  
  
5. DSL kitaplığı proje tarafından oluşturulan derleme (DLL) başvuru DSL projeye ekleyin.  
  
6. Çözümü oluşturun.  
  
   DSL kitaplığı diğer tür kitaplıklarını içeri aktarabilirsiniz. Bir kitaplığı içeri aktardığınızda, içeri aktarmalarından DSL Gezgini'nde da otomatik olarak görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Etki Alanına Özgü bir Dili Tanımlama](../modeling/how-to-define-a-domain-specific-language.md)
