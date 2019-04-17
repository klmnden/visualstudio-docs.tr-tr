---
title: 'CA1726: Tercih edilen terimleri kullanın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- UsePreferredTerms
- CA1726
helpviewer_keywords:
- UsePreferredTerms
ms.assetid: 642b2acd-3a33-4d1f-b0a7-67073ae73be2
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 67dab4c732faa04af44800f740d78c4ce4f9dc80
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59664118"
---
# <a name="ca1726-use-preferred-terms"></a>CA1726: Tercih edilen terimleri kullanın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA1726: Tercih edilen terimleri kullanın](https://docs.microsoft.com/visualstudio/code-quality/ca1726-use-preferred-terms).  
  
|||  
|-|-|  
|TypeName|UsePreferredTerms|  
|CheckId|CA1726|  
|Kategori|Microsoft.Naming|  
|Yeni Değişiklik|-Derlemelerini tetiklendiğinde sonu<br /><br /> Tür parametrelerinde tetiklendiğinde bölünemez-|  
  
## <a name="cause"></a>Sebep  
 Dışarıdan görünen bir tanımlayıcının adı, tercih edilen terim varolduğunda alternatif olarak bir terim içerir. Alternatif olarak, ad bayrağı veya bayrakları terim içerir.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bu kural, bir tanımlayıcı belirteçlere ayrıştırır. Her tek belirteç ve her bir bitişik belirteci çift bileşimi, kural ve özel sözlükler kullanım dışı bölümünde yerleşik koşulları karşılaştırılır. Aşağıdaki tabloda, kural ve kendi tercih edilen alternatif yerleşik koşulları gösterir.  
  
|Eski terimi|Tercih edilen terim|  
|-------------------|--------------------|  
|`Arent`|`AreNot`|
|`Cancelled`|`Canceled`|
|`Cant`|`Cannot`|
|`ComPlus`|`EnterpriseServices`|
|`Couldnt`|`CouldNot`|
|`Didnt`|`DidNot`|
|`Doesnt`|`DoesNot`|
|`Dont`|`DoNot`|
|`Flag` veya `Flags`|Hiçbir değişiklik terimi yoktur. Kullanmayın.|
|`Hadnt`|`HadNot`|
|`Hasnt`|`HasNot`|
|`Havent`|`HaveNot`|
|`Indices`|`Indexes`|
|`Isnt`|`IsNot`|
|`LogIn`|`LogOn`|
|`LogOut`|`LogOff`|
|`Shouldnt`|`ShouldNot`|
|`SignOn`|`SignIn`|
|`SignOff`|`SignOut`|
|`Wasnt`|`WasNot`|
|`Werent`|`WereNot`|
|`Wont`|`WillNot`|
|`Wouldnt`|`WouldNot`|
|`Writeable`|`Writable`|
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Bu kural ihlalini düzeltmek için tercih edilen alternatif terimiyle terimi değiştirin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Yalnızca tanımlayıcı adını kasıtlıdır ve özgün terimi yerine tercih edilen terim özellikle ilgili bu kuraldan bir uyarıyı gizler.  
  
## <a name="related-rules"></a>İlgili kuralları  
 [Adlandırma Uyarıları](../code-quality/naming-warnings.md)
