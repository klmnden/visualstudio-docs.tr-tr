---
title: VS Shell dağıtımı
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 70f39dd23851a2ebc0a48afd05da54b0d8deb24a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62934307"
---
# <a name="vs-shell-deployment"></a>VS Shell dağıtımı

Bir yalıtılmış Kabuk hangi Visual Studio belirlemenize olanak tanır işlevselliğe gereksinim, etki alanına özgü dil ve bu çözümü nasıl görüneceğini ile etkileşim kurmak. Visual Studio yalıtılmış Kabuk hakkında daha fazla bilgi için bkz. [yalıtılmış Kabuğu özelleştirme](https://vspartner.com/pages/vsshells).

Bir Visual Studio Shell dağıtım hedefi olarak ayarlamak için:

1. İçinde **DslPackage** projesini açarsanız **source.extension.tt**.

2. Altında `<SupportedProducts>` ekleyin:

   ```xml
   <IsolatedShell Version="1.0">MyIsolatedShell</IsolatedShell>
   ```

   Değiştirin *MyIsolatedShell* yalıtılmış Kabuk paketinizin ada sahip.