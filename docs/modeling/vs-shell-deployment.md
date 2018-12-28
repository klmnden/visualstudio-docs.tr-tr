---
title: VS Shell dağıtımı
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
ms.openlocfilehash: 663e706dba9ec7b6479e3e9360ef8aa2d12b1400
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53739503"
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