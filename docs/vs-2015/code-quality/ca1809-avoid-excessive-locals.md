---
title: 'CA1809: aşırı yerel öğelerden Kaçın | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1809
- AvoidExcessiveLocals
helpviewer_keywords:
- AvoidExcessiveLocals
- CA1809
ms.assetid: 5c81ea43-cb49-448f-980f-a1dd9764043c
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1e019c79138ab635e056852df426c5060d46da0b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223905"
---
# <a name="ca1809-avoid-excessive-locals"></a>CA1809: Aşırı yerel öğelerden kaçın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|AvoidExcessiveLocals|
|CheckId|CA1809|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Üye bazıları derleyici tarafından oluşturulmuş olabilir, 64'ten fazla yerel değişkenler içerir.

## <a name="rule-description"></a>Kural Tanımı
 Olarak adlandırılan bellek yerine işlemci kayıttaki değeri depolamak için yaygın bir performans iyileştirmesidir olduğu *kayıt* değeri. Ortak dil çalışma zamanı enregistration için en fazla 64 yerel değişkenler olarak değerlendirir. Kaydedilme olmayan değişkenler yığına yerleştirilir ve işleme önce bir kayıt taşınması gerekir. Fırsat izin vermek için tüm yerel değişkenlerin kaydedilme alın, 64 yerel değişken sayısını sınırlayın.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için en fazla 64 yerel değişken kullanmak için uygulama yeniden düzenleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Performans sorunu değilse bu kuraldan bir uyarıyı bastırmak için veya kuralı devre dışı bırakmak için güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)



