---
title: VS Shell dağıtımı
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: bc86574b380e0a29042dcc1dc20851258c9f1bc3
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55033577"
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