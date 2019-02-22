---
title: 'DA0029: Desteklenmeyen CLR sürümü | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.29
- vs.performance.rules.DA0029
helpviewer_keywords:
- vs.performance.29
- vs.performance.DA0029
- vs.performance.rules.DA0029
ms.assetid: 76247259-c6f3-44c4-b3f9-d8dac16b5e0d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a3855b8975684b088b2838a866db36e6ec19e665
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56635546"
---
# <a name="da0029-unsupported-clr-version"></a>DA0029: Desteklenmeyen CLR sürümü

|||
|-|-|
|Kural Kimliği|DA0029|
|Kategori|Profil oluşturma araçları kullanım|
|Profil oluşturma yöntemi|Komut satırından profil oluşturma|
|İleti|Koleksiyon sırasında desteklenmeyen CLR sürümü algılandı. Yönetilen semboller düzgün çözülemiyor olabilir.|
|Kural türü|Bilgiler.|

## <a name="cause"></a>Sebep
 Kullanan bir uygulama profili çalıştığınız [!INCLUDE[net_v11_long](../profiling/includes/net_v11_long_md.md)] profil oluşturma araçları tarafından desteklenmiyor.

## <a name="rule-description"></a>Kural açıklaması
 Profil oluşturma araçlarından uygulama içinde çalışan yönetilen kod için simgeleri çözme mümkün olmayacaktır. Bu uyarı oluşur. Profil oluşturma araçlarından çalışmakta olan uygulamalar için yönetilen kodu sembol çözümlenemiyor [!INCLUDE[net_v11_long](../profiling/includes/net_v11_long_md.md)].

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Yok.