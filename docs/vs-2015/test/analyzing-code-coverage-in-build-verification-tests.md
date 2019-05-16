---
title: Derleme doğrulama testlerinde kod kapsamını çözümleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
ms.assetid: 59c07d15-511e-4fd0-b398-bde9d5ed00d9
caps.latest.revision: 10
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1dc7dceeaf94ef94a46da6836fea95ac94e49db7
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65686454"
---
# <a name="analyzing-code-coverage-in-build-verification-tests"></a>Derleme Doğrulama Testlerinde Kod Kapsamını Çözümleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Microsoft Visual Studio kod kapsamı analizi, kodunuzun ne kadarını otomatik sınamalarında gösterir. Daha fazla bilgi için [kullanarak kod kapsamı için belirlemek ne kadar kodun test](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md).  
  
 Kodunuzda denetlediğinizde, testiniz diğer ekip üyelerinden gelen diğer tüm testlerle birlikte yapı sunucusunda çalışır. (, Zaten bu ayarları yapmadıysanız bkz [yapı işleminizde testler](https://msdn.microsoft.com/library/d05743a1-c5cf-447e-bed9-bed3cb595e38).) Kapsam tüm projeye en güncel ve en kapsamlı resmi sağladığından kod kapsamını yapı hizmetinde çözümlemek yararlıdır. Otomatik sistem testleri ve geliştirme makinelerinde genellikle çalıştırmadığınız kodlanmış diğer testleri de içerecektir.  
  
1. Takım Gezgini'nde açın **yapılar**ve ardından eklemek veya bir yapı tanımını düzenleyin.  
  
2. Üzerinde **işlem** sayfasında **otomatik testler**, **Test kaynağı**, **çalıştırma ayarları**. Ayarlama **çalışma ayarları dosya türü** için **kod kapsamı etkinleştirmesiyle**.  
  
    Birden fazla Test Kaynağı tanımı varsa, her biri için bu adımı yineleyin.  
  
   - <em>Adlı bir alan yoktur ancak **türü çalışma ayarları dosya</em>*. *  
  
      Altında **otomatik testler**seçin **Test derlemesi** ve üç nokta düğmesini **[...]**  satırın sonunda. İçinde **Test çalışmasını Ekle/Düzenle** iletişim kutusunun **Test Çalıştırıcısı**, seçin **Visual Studio Test Çalıştırıcısı**.  
  
   ![Derleme tanımı için kod kapsamı ayarlama](../test/media/codecoverage-plaincc.png "CodeCoverage plainCC")  
  
   Yapı çalıştıktan sonra kod kapsamı sonuçları yapı Özet olarak görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ne Kadar Kodun Test Edildiğini Belirlemek için Kod Kapsamını Kullanma](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md)
