---
title: 'CA1822: Üyeleri statik olarak işaretleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- MarkMembersAsStatic
- CA1822
helpviewer_keywords:
- MarkMembersAsStatic
- CA1822
ms.assetid: 743f0af7-41d1-4852-8d97-af0688b31118
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 42c6f0d333d1f7ee3f657b9c57c4154e9f824128
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59659780"
---
# <a name="ca1822-mark-members-as-static"></a>CA1822: Üyeleri static olarak işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1822: Üyeleri statik olarak işaretlemek](https://docs.microsoft.com/visualstudio/code-quality/ca1822-mark-members-as-static).  
  
|||  
|-|-|  
|TypeName|MarkMembersAsStatic|  
|CheckId|CA1822|  
|Kategori|Microsoft.Performance|  
|Yeni Değişiklik|Bölünemez - üyesi derlemenin dışında görünür değilse bağımsız olarak, değişiklik.<br /><br /> Örnek üyesine ile üye yalnızca değiştirirseniz bölünemez - `this` anahtar sözcüğü.<br /><br /> -Üye statik bir üyeye bir örnek üyesi değiştirirseniz ve derlemenin dışında görünür kesiliyor.|  
  
## <a name="cause"></a>Sebep  
 Örnek veri erişimi olmayan bir üye statik olarak işaretlenmemiş (paylaşılan [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]).  
  
## <a name="rule-description"></a>Kural Tanımı  
 Örnek veri veya çağrı örnek yöntemlerinin erişmez üyeleri işaretlenebilir olarak statik (paylaşılan [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]). Yöntemleri statik olarak işaretledikten sonra, derleyici sanal olmayan arama sitelerini bu üyelere yayar. Sanal olmayan arama sitelerini yayma, geçerli nesne işaretçisinin null dışında değer xenapp'i her çağrı çalışma zamanında bir onay engeller. Bu, ölçülebilir kazanç performansını performans duyarlı kodunuz için elde edebilirsiniz. Bazı durumlarda geçerli nesne örneğine erişmek için başarısızlık, bir doğruluk sorununu temsil eder.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Üye statik olarak işaretleyin (veya paylaşılan [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) veya 'this' kullanma / yönteminde ' Me' body, uygun olduğunda.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Daha önce sevk edilen kod düzeltme bir değişiklik olur için bu kuraldan bir uyarıyı bastırmak güvenlidir.  
  
## <a name="related-rules"></a>İlgili kuralları  
 [CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)  
  
 [CA1812: Örneklenmemiş iç sınıflardan kaçının](../code-quality/ca1812-avoid-uninstantiated-internal-classes.md)  
  
 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)
