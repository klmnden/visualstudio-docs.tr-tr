---
title: 'CA1900: Değer tür alanları taşınabilir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1900
- ValueTypeFieldsShouldBePortable
helpviewer_keywords:
- ValueTypeFieldsShouldBePortable
- CA1900
ms.assetid: 1787d371-389f-4d39-b305-12b53bc0dfb9
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 97a83bf4ba71d0adc71fdb96d4e1c865358c08e2
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59665760"
---
# <a name="ca1900-value-type-fields-should-be-portable"></a>CA1900: Değer tür alanları taşınabilir olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1900: Değer tür alanları taşınabilir](https://docs.microsoft.com/visualstudio/code-quality/ca1900-value-type-fields-should-be-portable).  
  
|||  
|-|-|  
|TypeName|ValueTypeFieldsShouldBePortable|  
|CheckId|CA1900|  
|Kategori|Microsoft.Portability|  
|Yeni Değişiklik|Alan derlemesi dışında görülebilir, - kesiliyor.<br /><br /> Bölünemez - alanın derlemenin dışında görünür değilse.|  
  
## <a name="cause"></a>Sebep  
 Bu kural ile açık düzene bildirilen yapıları için 64-bit işletim sistemlerinde yönetilmeyen kod sıralandığı zaman doğru olarak hizalamayı denetler. IA-64 hizalanmamış bellek erişir ve bu ihlal düzeltilmezse süreci kilitlenecek izin vermez.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Sahip 64 bit işletim sistemlerinde Çökmelere neden olur yanlış hizalanmış alanlar içeren açık Yerleşimli yapılar.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 8 bayttan küçük olan tüm alanlar, boyutunun bir katı olan uzaklık ve 8 bayt alanlar olmalıdır veya daha fazla 8'in katı olan uzaklık olması gerekir. Başka bir çözüm `LayoutKind.Sequential` yerine `LayoutKind.Explicit`makul verilebilir.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Bu uyarı yalnızca hata oluşursa atlanması.
