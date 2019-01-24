---
title: Etki alanı ilişkilerinin özellikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, domain relationships
ms.assetid: 9ccb3dc2-b80c-4585-932f-3c5f87bafbcd
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 56deef795d1b48dc1b49d8ab255fc7a4fbf7379e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54767327"
---
# <a name="properties-of-domain-relationships"></a>Etki Alanı İlişkilerinin Özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Özellikler aşağıdaki tabloda, bir etki alanı ilişkisi ile ilişkilendirilir. Etki alanı ilişkileri hakkında daha fazla bilgi için bkz: [anlama modelleri, sınıfları ve ilişkileri](../modeling/understanding-models-classes-and-relationships.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|Erişim değiştiricisi|Alan ilişkisine ait erişim düzeyini (`public` veya `internal`).|`public`|  
|Özel Öznitelikler|Etki alanına ilişkisinden oluşturulan kaynak kod sınıfı öznitelikler eklemek için kullanılır.|\<yok >|  
|Çift oluşturur türetilmiş|Varsa `True`, hem temel sınıf hem de (geçersiz kılmalar aracılığıyla özelleştirmeyi desteklemek için) bir kısmi sınıf oluşturulur. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|`False`|  
|Özel oluşturucu vardır.|Varsa `True`, özel bir oluşturucu kaynak kodunda sağlandığını belirtir. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|`False`|  
|Devralma değiştiricisi|Etki alanına ilişkisinden oluşturulan kaynak kodu sınıf devralma türü açıklar (`none`, `abstract` veya `sealed`).|\<yok >|  
|Yinelenen sağlar|Varsa `True`, etki alanı ilişkisine ait yinelenen bağlantıların aynı iki öğe oluşturulabilir.|`False`|  
|Temel ilişki|Etki alanı ilişkisi türetilmişse, etki alanı ilişkisinin temel ilişkisi.|\<yok >|  
|Gömme olduğu|Varsa `True`, etki alanı ilişki gömme ilişkisi vardır. Varsa `False`, bir başvuru ilişkisi ilişkidir.|\<her ikisi de >|  
|Ad|Etki alanı ilişkisi adı.|Geçerli ad|  
|Ad Alanı|Etki alanı ilişkisi ile bağlantılı olan ad alanı.|Geçerli ad alanı|  
|Notlar|Etki alanı ilişkisi ile ilişkili resmi olmayan notlar.|\<yok >|  
|Açıklama|Kod belge için kullanılır ve oluşturulan tasarımcının kullanıcı Arabiriminde kullanılan açıklaması.|\<yok >|  
|Görünen Ad|Etki alanı ilişkisi için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|  
|Yardım anahtar sözcüğü|Etki alanı ilişkisi için F1 Yardımı dizini oluşturmak için kullanılan isteğe bağlı anahtar sözcük.|\<yok >|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
