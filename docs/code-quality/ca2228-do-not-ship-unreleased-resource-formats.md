---
title: 'CA2228: Yayımlanmamış kaynak biçimlerini yollamayın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotShipUnreleasedResourceFormats
- CA2228
helpviewer_keywords:
- CA2228
- DoNotShipUnreleasedResourceFormats
ms.assetid: 2c614edc-4e94-4b4f-8067-eea677a75cd9
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 19f903ae02413bf18474aa2d95d71d765c288fa9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49900637"
---
# <a name="ca2228-do-not-ship-unreleased-resource-formats"></a>CA2228: Yayımlanmamış kaynak biçimlerini yollamayın

|||
|-|-|
|TypeName|DoNotShipUnreleasedResourceFormats|
|CheckId|CA2228|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir kaynak dosyası şu anda desteklenmeyen bir .NET Framework sürümü kullanılarak oluşturuldu.

## <a name="rule-description"></a>Kural açıklaması
 .NET Framework'ün yayın öncesi sürümleri kullanılarak oluşturulan kaynak dosyaları .NET Framework'ün desteklenen sürümleri tarafından kullanılamayabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için .NET Frameworkk desteklenen bir sürümünü kullanarak kaynak oluşturun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.