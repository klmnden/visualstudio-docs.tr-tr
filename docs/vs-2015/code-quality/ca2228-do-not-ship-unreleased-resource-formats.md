---
title: 'CA2228: Yayımlanmamış kaynak biçimlerini yollamayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotShipUnreleasedResourceFormats
- CA2228
helpviewer_keywords:
- CA2228
- DoNotShipUnreleasedResourceFormats
ms.assetid: 2c614edc-4e94-4b4f-8067-eea677a75cd9
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2e49953a95da10653cd29132e003fa36de5b8d4c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142434"
---
# <a name="ca2228-do-not-ship-unreleased-resource-formats"></a>CA2228: Yayımlanmamış kaynak biçimlerini yollamayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotShipUnreleasedResourceFormats|
|CheckId|CA2228|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir kaynak dosyası bir sürümü kullanılarak oluşturulmuş [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] , şu anda desteklenmiyor.

## <a name="rule-description"></a>Kural Tanımı
 Yayın öncesi sürümlerini kullanarak oluşturulan kaynak dosyaları [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] desteklenen .NET Framework sürümleri tarafından kullanılamayabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için desteklenen bir sürümünü kullanarak kaynak oluşturma [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]k.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.
