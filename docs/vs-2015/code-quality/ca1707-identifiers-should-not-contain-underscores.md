---
title: 'CA1707: Tanımlayıcılar alt çizgi içermemelidir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotContainUnderscores
- CA1707
helpviewer_keywords:
- CA1707
- IdentifiersShouldNotContainUnderscores
ms.assetid: 5fb539ef-c304-4323-90c0-b14386da9774
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 8ae59f396115f10a858c5bc31d8bcdbf967d1d80
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355103"
---
# <a name="ca1707-identifiers-should-not-contain-underscores"></a>CA1707: Tanımlayıcılar alt çizgi içermemelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1707: Tanımlayıcılar alt çizgi içermemelidir](https://docs.microsoft.com/visualstudio/code-quality/ca1707-identifiers-should-not-contain-underscores) docs.microsoft.com'da.  
  
|||  
|-|-|  
|TypeName|IdentifiersShouldNotContainUnderscores|  
|CheckId|CA1707|  
|Kategori|Microsoft.Naming|  
|Yeni Değişiklik|-Derlemelerini oluştuğunda kesme<br /><br /> Tür parametrelerinde oluştuğunda bölünemez-|  
  
## <a name="cause"></a>Sebep  
 Bir tanımlayıcının adı alt çizgi (_) karakterini içeriyor.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Kural gereği, tanımlayıcı adlar alt çizgi (_) karakterini içermez. Kural ad alanlarını, türleri, üyeleri ve parametreleri denetler.  
  
 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Tüm alt çizgi karakterleri adından kaldırın.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Bu kuraldan uyarıyı bastırmayın.  
  
## <a name="related-rules"></a>İlgili kuralları  
 [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)  
  
 [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
