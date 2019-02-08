---
title: Taşınabilirlik Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.PortabilityRules
helpviewer_keywords:
- portability warnings
- managed code analysis warnings, portability warnings
- warnings, portability
ms.assetid: 902e859a-2153-4970-baaa-8a5b4a11806f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a6a3557cffec60de91da46f60040ec675c866cbf
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55946610"
---
# <a name="portability-warnings"></a>Taşınabilirlik Uyarıları
Taşınabilirlik uyarıları, farklı işletim sistemleri arasında taşınabilirlik destekler.

## <a name="in-this-section"></a>Bu Bölümde

|Kural|Açıklama|
|----------|-----------------|
|[CA1900: Değer tür alanları taşınabilir olmalıdır](../code-quality/ca1900-value-type-fields-should-be-portable.md)|Bu kural açık düzene özniteliği kullanılarak bildirilen yapıları için 64-bit işletim sistemlerinde yönetilmeyen kod sıralandığı zaman doğru hizalamayı denetler.|
|[CA1901: P/Invoke bildirimleri taşınabilir olmalıdır](../code-quality/ca1901-p-invoke-declarations-should-be-portable.md)|Bu kural her parametresinin boyutu ve P/Invoke dönüş değeri değerlendirir ve bunların boyutu 32-bit ve 64-bit işletim sistemlerinde yönetilmeyen kodun başvuruya doğru olduğunu doğrular.|
|[CA1903: Yalnızca hedeflenen çerçeveden API kullanın](../code-quality/ca1903-use-only-api-from-targeted-framework.md)|Bir üye veya tür, bir üye veya projedeki hedeflenen çerçeve ile birlikte dahil edilmemiş hizmet paketinde tanıtılmış türü kullanır.|