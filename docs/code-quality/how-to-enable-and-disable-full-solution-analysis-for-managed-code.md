---
title: 'Nasıl yapılır: Yönetilen kod için tam çözüm analizini devre dışı bırakma ve etkinleştirme'
ms.date: 03/23/2018
ms.topic: conceptual
helpviewer_keywords:
- full solution analysis
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: dbd4cf06a5d51a668acc5c980e7e93a94f2992f2
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55931006"
---
# <a name="how-to-enable-and-disable-full-solution-analysis-for-managed-code"></a>Nasıl yapılır: Yönetilen kod için tam çözüm analizini devre dışı bırakma ve etkinleştirme

*Tam çözüm analizini* Kod Analizi sorunlarını yalnızca açık görseldeki görmenize olanak sağlayan bir Visual Studio özellik C# veya Visual Basic dosyaları çözümünüzdeki veya kod dosyalarında kapatılır. Varsayılan olarak, tam çözüm analizini olan *etkin* Visual Basic ve *devre dışı* görsel için C#.

Tüm dosyalardaki tüm sorunları görmek yararlı olabilir, ancak ayrıca dikkat dağıtıcı olabilir. Çözümünüzü çok büyük veya çok sayıda dosya varsa, bir Visual Studio yavaşlar. Gösterilen sorunların sayısını sınırlayabilir ve Visual Studio performansını artırmak için tam çözüm analizini devre dışı bırakabilirsiniz. Bu özellik, gerekirse kolayca etkinleştirebilirsiniz.

## <a name="to-toggle-full-solution-analysis"></a>Tam çözüm analizini açıp kapatmak için

1. Açmak için **seçenekleri** Seç iletişim kutusu, Visual Studio'da menü çubuğunda **Araçları** > **seçenekleri**.

1. İçinde **seçenekleri** iletişim kutusunda **metin düzenleyici**  >  **C#** veya **temel**  >  **Gelişmiş**.

1. Seçin **tam çözüm analizini etkinleştirme** onay kutusunu tam çözüm analizini etkinleştirme veya devre dışı bırakmak için onay kutusunu temizleyin. Seçin **Tamam** bitirdiğinizde.

    ![Tam çözüm analizi onay kutusunu etkinleştirin.](../code-quality/media/options-enable-full-solution-analysis.png)

## <a name="results-of-enabling-and-disabling-full-solution-analysis"></a>Sonuçlarını tam çözüm analizini devre dışı bırakma ve etkinleştirme

Tam çözüm analizini etkin olduğunda, aşağıdaki ekran görüntüsünde, sonuçlarını görebilirsiniz. Tüm hataları ve Kod Analizi sorunlarıyla *tüm* dosyaların Çözümdeki dosyalar veya açık olup bağımsız olarak görünür.

![Tam çözüm analizini etkin.](../code-quality/media/fsa_enabled.png)

Aşağıdaki ekran görüntüsünde, tam çözüm analizini devre dışı bıraktıktan sonra aynı çözümünden alınan sonuçları gösterir. Yalnızca hataları ve Kod Analizi sorunlarına çözüm Aç dosyalarında görünür **hata listesi**.

![Tam çözüm analizini devre dışı.](../code-quality/media/fsa_disabled.png)

## <a name="automatically-disable-full-solution-analysis"></a>Otomatik olarak tam çözüm analizini devre dışı bırak

Visual Studio algılarsa 200 MB veya daha az sistem belleği için kullanılabilir, etkinleştirildiğinde, otomatik olarak tam çözüm analizini (ve diğer bazı özellikleri) devre dışı bırakır. Bu meydana gelirse, Visual Studio bazı özellikler devre dışı olduğunu bildiren bir uyarı görünür. Bir düğme istiyorsanız tam çözüm analizini etkinleştirme olanak tanır.

![Tam çözüm analizini askıya uyarı metni](../code-quality/media/fsa_alert.png)