---
title: Paket yüklerini sürümünden sonra ne zaman değişir?
description: Bir düzen oluştururken bir sürümü kullanıma sunulduktan sonra paket yüklerini değişmesi gerekmediğini belirleme hakkında bilgi edinin.
ms.date: 05/22/2019
ms.topic: conceptual
author: et13
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 6a4eb286344b6dce7a4814089db013965eb34c98
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66411161"
---
# <a name="package-payload-changes"></a>Paket yükü değişiklikleri

Bazı paket yüklerini bir sürümü kullanıma sunulduktan sonra değiştirmek için izin verilir. Bir düzen veya bir başkasının oluşturduğu zaman, bu davranışı bir düzen oluşturulduğu bağlı olarak farklı bir düzen içerik neden olabilir.

## <a name="verify-that-a-layout-includes-package-payload-changes"></a>Bir düzen paket yükü değişiklikler içerdiğini doğrulayın

Önceden oluşturulmuş düzen bir sürüm kullanıma sonra değiştirilen paket yüklerini almışsa belirlemek nasıl aşağıda verilmiştir:

1. Kurulum günlüğü'nü açın. Altındadır genellikle günlük `%TEMP%\dd_setup_[date].log` burada `[date]` Düzen işlemi başlatılan ise `yyyyMMddHHmmss` biçimi.

2. Bir satırda şu metin gibi yapılandırılmış günlük ara:

    `Falling back to signature and signer check because hash verification returned HashMismatch for path: [path]`

3. Ardından, indirme [yol] için başarılı olduğunu gösteren satırlarında daha sonra günlük arayın. Bunlar aşağıdaki metne benzer görünebilir:

    `Download of [url] succeeded using engine 'WebClient'`

    `END: Downloading [url] to [path]`

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'nun bir ağ oluşturun](create-a-network-installation-of-visual-studio.md)
* [Visual Studio'nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)