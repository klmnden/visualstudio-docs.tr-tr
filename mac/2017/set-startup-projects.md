---
title: Mac için Visual Studio Çoklu Başlangıç projeleri ayarlama
description: Bu makalede, çalıştırma veya hata ayıklama başlatmak için birden çok proje ayarlama açıklanır.
author: sayedihashimi
ms.author: sayedha
ms.date: 02/21/2019
ms.topic: conceptual
ms.prod: visual-studio-mac
ms.assetid: fd354fff-ce6b-4505-a815-84a2311e39ba
ms.openlocfilehash: a4a4f2f4fd4ce6cd88d11979a21e4e9184adfca8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62988444"
---
# <a name="how-to-set-multiple-startup-projects"></a>Nasıl yapılır: Çoklu başlangıç projeleri ayarlama

Mac için Visual Studio belirtmenize olanak verir nasıl birden çok hata ayıklama veya çalıştırdığınızda, çözümünüze bir proje başlatılır.

## <a name="to-set-multiple-startup-projects"></a>Birden fazla başlangıç projesi olarak ayarlamak için

1. İçinde **çözüm bölmesi**, ' % s'çözümü (üst düğümü) seçin.

2. Çözüm düğümün (sağ tıklama) bağlam menüsünü seçin ve ardından **başlangıç projelerini Ayarla...** .

   ![Kümesi başlangıç projeleri bağlam menüsü](media/startup-proj-ctx-menu.png)

3. **Çözüm çalıştırma yapılandırması oluşturun** iletişim kutusu görüntülenir. Bu iletişim için yeni bir adlandırılmış çözüm çalıştırma yapılandırma çözümünüzü oluşturacaksınız. Herhangi bir ad verebilirsiniz istediğiniz, varsayılan ad `Multiple Projects`.

   ![Çözüm çalıştırma yapılandırma iletişim kutusu oluşturma](media/create-sln-run-config.png)

4. Tıklayın **çalıştırma yapılandırması oluşturun**. **Çözüm seçenekleri** yeni çözüm çalıştırma seçili yapılandırma ile iletişim kutusu açılır.

   ![Çözüm Seçenekleri iletişim kutusu](media/sln-options-run-config-multi-projects.png)

5. Hata ayıklama veya çalıştırdığınızda, Mac için Visual Studio uygulamanızı başlatmak istediğiniz projeleri seçin

   ![Çözüm Seçenekleri iletişim kutusu ile yapılandırılmış bir çalıştırma yapılandırma](media/sln-options-run-config-multi-projects-configured.png)

6. **Tamam**'ı tıklatın. İletişim kutusu kapatıldı ve çalıştırma yeni çözüm yapılandırması etkin çalışma yapılandırması ayarlanır.

   ![Hata ayıklamayı başlatmak veya çalıştırmak için yapılandırılmış birden çok proje çözümüyle](media/startup-project-configured.png) iki proje hem projede olduğundan başlatmak için yapılandırıldığını görebilirsiniz **kalın** içinde **çözüm bölmesi**. Araç çubuğunda, yeni bir çalıştırma yapılandırma geçerli çözüm çalıştırma yapılandırması yapılandırılır.

## <a name="next-steps"></a>Sonraki adımlar

- [Derleme ve Mac için Visual Studio'da oluşturma](compiling-and-building.md)
- [Derleme yapılandırmalarını anlama](configurations.md)