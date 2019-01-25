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
ms.openlocfilehash: bf1050716bb38f8b43aa8be7d88c474960544b2d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770540"
---
# <a name="ca1726-use-preferred-terms"></a>CA1726: Tercih edilen terimleri kullanın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 2017 ile ilgili en son belgeler için bkz. [CA1726: Tercih edilen terimleri kullanın](https://docs.microsoft.com/visualstudio/code-quality/ca1726-use-preferred-terms) docs.microsoft.com'da.  
  
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
|değil|Gereksinim yoktur|  
|İptal Edildi|İptal edildi|  
|İşlenemedi|Olamaz|  
|ComPlus|EnterpriseServices|  
|Sonucun|CouldNot|  
|Didnt|DidNot|  
|Doesnt|DoesNot|  
|Yok|DoNot|  
|Bayrağı veya bayrakları|Hiçbir değişiklik terimi yoktur. Kullanmayın.|  
|yüklediniz|HadNot|  
|Henüz|HasNot|  
|henüz|HaveNot|  
|Dizinleri|Dizinleri|  
|değil|IsNot|  
|Oturum açma|Oturum açma|  
|Oturum kapatma|Oturumu Kapat|  
|Shouldnt|ShouldNot|  
|Oturum açma|Oturum açma|  
|Oturumu kapatma|Oturum kapatma|  
|Wasnt|WasNot|  
|derlemedeki|WereNot|  
|Yapmıyor|WillNot|  
|Wouldnt|Görmeyecektir|  
|Yazılabilir|Yazılabilir|  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Bu kural ihlalini düzeltmek için tercih edilen alternatif terimiyle terimi değiştirin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Yalnızca tanımlayıcı adını kasıtlıdır ve özgün terimi yerine tercih edilen terim özellikle ilgili bu kuraldan bir uyarıyı gizler.  
  
## <a name="related-rules"></a>İlgili kuralları  
 [Adlandırma Uyarıları](../code-quality/naming-warnings.md)
