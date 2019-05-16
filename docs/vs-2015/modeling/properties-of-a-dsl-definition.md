---
title: Bir DSL tanımının özellikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, definition file
ms.assetid: 38debcfe-e1a6-4a3f-9d69-3ab07520f2b6
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 77f0a384797217440600d1ba5db0f190f4bdafa3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65685359"
---
# <a name="properties-of-a-dsl-definition"></a>DSL Tanımının Özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DslDefinition özelliklerini tanımlayın *etki alanına özgü dil* sürümü numaralandırma gibi tanımı özellikleri. DslDefinition özellikleri görünür **özellikleri** pencere, diyagramdaki boş bir alanı tıkladığınızda *etki alanına özgü dil tasarımcısını*.  
  
 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
 DslDefinition aşağıdaki tabloda özelliklere sahiptir:  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|Erişim değiştiricisi|Alan sınıfına ait erişim değiştiricisinin public veya internal olduğunu belirler.|public|  
|Özel Öznitelikler|Özel öznitelikler etki alanı sınıfı için tanımlanmış.<br /><br /> **Not** bir öznitelik eklemek için Gözat düğmesini kullanın.|\<yok >|  
|Şirket adı|Sistem kayıt defterinde geçerli şirket adı adı.|Geçerli bir şirket adı|  
|Ad|Bu alan sınıfının adı.|Geçerli ad|  
|Ad Alanı|Bu alan sınıfıyla ilişkili ad alanı.|Geçerli ad alanı|  
|Paket GUID'si|GUID [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] bu DSL için oluşturulan paket.|\<yok >|  
|Paket Namespace|Ad alanı için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] bu DSL için oluşturulan paket.|\<yok >|  
|Ürün Adı|İçin kaydedilen ürün adını [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] bu DSL için oluşturulan paket.|\<yok >|  
|Notlar|Bu alan sınıfıyla ilişkili notları.|\<yok >|  
|Açıklama|Bu etki alanı sınıfı için açıklama.|\<yok >|  
|Görünen Ad|Bu etki alanı sınıfı için oluşturulan tasarımcıda görüntülenecek ad.|\<yok >|  
|Yardım anahtar sözcüğü|Bu alan sınıfıyla ilişkili Yardım anahtar sözcüğü.|\<yok >|  
|Yapı|Bu etki alanına özgü dil tanımı için artımlı derleme numarası.|0|  
|Ana sürüm|Bu etki alanına özgü dil tanımı için artımlı başlıca yapı numarası.|1.|  
|Alt sürüm|Bu etki alanına özgü dil tanımı için artımlı alt yapı numarası.|0|  
|Gözden geçirme|Artımlı düzeltme numarası için bu etki alanına özgü dil tanımı oluşturun.|0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
