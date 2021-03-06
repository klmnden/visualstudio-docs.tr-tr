---
title: Diyagramların özellikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
f1_keywords:
- vs.dsltools.dsldesigner.dsldiagram
helpviewer_keywords:
- Domain-Specific Language, diagram
ms.assetid: 00bba4b8-6aa6-4027-96cb-4f4c41a77d3c
caps.latest.revision: 27
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7d669d01339b92c64cfe03ccb3ae897a1816aeac
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701754"
---
# <a name="properties-of-diagrams"></a>Diyagramların Özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Diyagramları oluşturulan tasarımcıdaki nasıl görüntüleneceğini belirten özellikleri ayarlayabilirsiniz. Örneğin, bir metin için varsayılan rengi diyagramda belirtebilirsiniz.  
  
 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
 Aşağıdaki tabloda, diyagramların özellikleri listeler.  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|Dolgu rengi|Diyagramın dolgu rengi.|Beyaz|  
|Metin rengi|Diyagram üzerinde görüntülenen metnin rengi.|Siyah|  
|Erişim değiştiricisi|Erişim değiştiricisi bir sınıfın (public veya internal).|Ortak|  
|Özel Öznitelikler|Oluşturulan kodun sınıf için öznitelikleri eklemek için kullanılır.|\<yok >|  
|Çift oluşturur türetilmiş|Varsa `True`, hem temel sınıf hem de (geçersiz kılmalar aracılığıyla özelleştirmeyi desteklemek için) bir kısmi sınıf oluşturulur. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md).|False|  
|Özel oluşturucu vardır.|Varsa `True`, kaynak kodunda özel bir oluşturucu sağlanacaktır. Daha fazla bilgi için [geçersiz kılma ve oluşturulan sınıflar genişletme](../modeling/overriding-and-extending-the-generated-classes.md)...|False|  
|Devralma değiştiricisi|Devralma diyagramından oluşturulan kaynak kodu sınıf türünü açıklar (`none`, `abstract` veya `sealed`).|Yok.|  
|Temel Diyagram|Bu diyagram, temel sınıf.|(hiçbiri)|  
|Ad|Bu diyagram adı.|Geçerli ad|  
|Ad Alanı|Bu diyagram ile bağlantılı olan ad alanı.|Geçerli ad alanı|  
|Temsil edilen sınıf|Bu diyagramda temsil eden kök etki alanı sınıfı.|Varsa geçerli kök sınıfı|  
|Notlar|Bu öğeyle ilişkili resmi olmayan notlar.|\<yok >|  
|Özellik olarak kullanıma sunan dolgu rengi|Varsa `True`, kullanıcı oluşturulan tasarımcının diyagramın dolgu rengi ayarlayabilirsiniz. Bunu ayarlamak için diyagramda şekle sağ tıklayın ve **ekleme Explosed**.|False|  
|Metin rengi özellik olarak kullanıma sunar.|Varsa `True`, kullanıcı diyagramda metin rengini oluşturulan tasarımcıdaki ayarlayabilirsiniz. Bunu ayarlamak için diyagramda şekle sağ tıklayın ve **ekleme Explosed**.|False|  
|Açıklama|Oluşturulan tasarımcının belgelemek için kullanılan bir açıklaması.|\<yok >|  
|Görünen Ad|Bu diyagram için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|  
|Yardım anahtar sözcüğü|Bu diyagram için F1 Yardımı dizini oluşturmak için kullanılan anahtar sözcüğü.|\<yok >|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
