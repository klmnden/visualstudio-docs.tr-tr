---
title: Kod çözümleme iade ilkeleri için sürüm uyumluluğu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- version compatibility, code analysis check-in policy
- check-in policies, version compatibility for code analysis
ms.assetid: 1af376e3-3be7-4445-803b-76a858567a5b
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0a63ead03baffaa0ce8047220ff1ce8a33c88be8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201161"
---
# <a name="version-compatibility-for-code-analysis-check-in-policies"></a>Kod Analizi İade İlkeleri için Sürüm Uyumluluğu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Değerlendirmek ve kod çözümleme iade ilkeleri farklı sürümlerini kullanan Yazar [!INCLUDE[esprtfc](../includes/esprtfc-md.md)], nasıl farkları bilmeniz gerekir [!INCLUDE[vstsTfsOrcasLong](../includes/vststfsorcaslong-md.md)] ve [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] iade ilkelerini değerlendirme.  
  
## <a name="version-compatibility-for-evaluating-check-in-policies"></a>İade ilkelerini değerlendirme için sürüm uyumluluğu  
  
- Ne zaman kod çözümleme iade ilkeleri değerlendirilir [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], varolan herhangi bir kuralın [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] ancak içinde yok [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] göz ardı edilir.  
  
- Ne zaman kod çözümleme iade ilkeleri değerlendirilir [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], özel olan tüm yeni kuralları [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] göz ardı edilir.  
  
- Kod çözümleme iade ilkesi kuralları derlemeleri belirtiyorsa [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] tarafından tanınmayan derlemeler tarafından belirtilen tüm kuralları yok sayar.  
  
- Kod çözümleme iade ilkesi kuralları derlemeleri belirtirse, [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] tanımıyor, bir ileti görüntülenir.  
  
## <a name="version-compatibility-for-authoring-check-in-policies"></a>İade ilkeleri yazmak için sürüm uyumluluğu  
  
- İade Kod Analizi İlkesi kullanarak oluşturduysanız [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] sürümünü [!INCLUDE[esprtfc](../includes/esprtfc-md.md)], kullanamazsınız [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] sürümünü [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] değiştirmek için. Ayrıca, [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] ilke değerlendirilemiyor.  
  
- İade Kod Analizi İlkesi kullanarak oluşturduysanız [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] içinde [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], kullanabileceğiniz [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] içinde [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] ve ilkeyi değiştirmek için de göre değerlendirilebilir [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)]. İlkeyi kullanarak değiştirdikten sonra [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] içinde [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], ilkeyi kullanarak artık düzenleyemezsiniz [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] içinde [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)]. [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] eşleşmeyen tanımlayıcı adlarla sorunsuz ilkeleri değerlendirebilirsiniz.  
  
- Kod Analizi İlkesi iade için her ikisinin de geçerli kural ayarları oluşturmak için [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] ve [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], ilke oluşturmalıdır [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], gerekli tüm değişiklikleri yapın ve ilkeyi kaydedin. Kuralları yapılan değişiklikler yalnızca varsa [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], değiştirebilir ve ilke kaydetme [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)].  
  
     İlkeyi kaydettikten sonra [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], artık mevcut kurallarına yönelik ayarları değiştirebilirsiniz [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] yalnızca.
