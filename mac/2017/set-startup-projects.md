---
title: Mac için Visual Studio Çoklu Başlangıç projeleri ayarlama
description: Bu makalede, çalıştırma veya hata ayıklama başlatmak için birden çok proje ayarlama açıklanır.
author: sayedihashimi
ms.author: sayedha
ms.date: 02/21/2019
ms.topic: conceptual
ms.prod: visual-studio-mac
ms.assetid: fd354fff-ce6b-4505-a815-84a2311e39ba
ms.openlocfilehash: c692cf8907fcd232b7ba442cea351664bc8dd407
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043605"
---
# <a name="set-multiple-startup-projects"></a>Çoklu başlangıç projeleri ayarlama

Mac için Visual Studio, hata ayıklama veya çözümünüzü çalıştırdığınızda birden fazla proje başlaması gerektiğini belirtmenize olanak sağlar.

## <a name="to-set-multiple-startup-projects"></a>Birden fazla başlangıç projesi olarak ayarlamak için

1. Çözüm panelinde, ' % s'çözümü (üst düğümü) seçin.

2. Çözüm düğümüne sağ tıklayın ve ardından **başlangıç projelerini Ayarla**:

   ![Başlangıç projeleri kümesi seçin](media/startup-proj-ctx-menu.png)

3. **Çözüm çalıştırma yapılandırması oluşturun** iletişim kutusu açılır. Bu iletişim kutusu için yeni bir adlandırılmış çözüm çalıştırma yapılandırma çözümünüzü oluşturmanıza olanak sağlar. İstediğiniz herhangi bir ad kullanabilirsiniz. Varsayılan ad `Multiple Projects`.

   ![Çözüm çalıştırma yapılandırması iletişim kutusu oluşturma](media/create-sln-run-config.png)

4. Seçin **çalıştırma yapılandırması oluşturun**. **Çözüm seçenekleri** yeni çözüm çalıştırma seçili yapılandırma ile iletişim kutusu açılır:

   ![Çözüm Seçenekleri iletişim kutusu](media/sln-options-run-config-multi-projects.png)

5. Hata ayıklama veya uygulamanızı Mac için Visual Studio'dan çalıştırma başlatmak istediğiniz projeleri seçin:

   ![Seçilen projeler çözüm Seçenekleri iletişim kutusu](media/sln-options-run-config-multi-projects-configured.png)

6. **Tamam**’ı seçin. Yeni çözüm yapılandırması çalıştırmak, etkin çalışma yapılandırması ayarlanır:

   ![İle hata ayıklamayı başlatmak veya çalıştırmak için yapılandırılmış birden çok proje çözümü](media/startup-project-configured.png)

   İki proje çünkü her iki proje başlatmak için yapılandırıldığını görebilirsiniz **kalın** çözüm panelinde. Araç çubuğunda, yeni bir çalıştırma yapılandırma geçerli çözüm çalıştırma yapılandırması ayarlanır.

## <a name="next-steps"></a>Sonraki adımlar

- [Derleme ve Mac için Visual Studio'da oluşturma](compiling-and-building.md)
- [Yapı yapılandırmalarını anlama](configurations.md)
