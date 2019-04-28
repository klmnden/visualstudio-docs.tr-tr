---
title: "Nasıl yapılır: Mac için Visual Studio'da birden fazla çözümü açın"
description: Mac için Visual Studio'da birden fazla çözümü açın ve uygulamanın birden fazla örneğini açmayı öğrenin.
author: conceptdev
ms.author: crdun
ms.date: 07/19/2018
ms.assetid: 592BA4E3-8DEF-4FCD-8BA0-519A4CEEE03E
ms.custom: video
ms.openlocfilehash: cdbe02cf3d60b460252f09764521afd240551115
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62988201"
---
# <a name="open-multiple-solutions-or-instances-of-visual-studio-for-mac"></a>Mac için birden fazla çözüm ya da Visual Studio örneklerini açın

Mac için Visual Studio da dahil olmak üzere bir Mac bilgisayarda varsayılan olarak, tüm uygulamalardır _Tek Örnekli_ uygulamalar. Bu, kullanmak istediğiniz uygulamayı (bir nokta dock'taki simgesinin altında tarafından gösterilen) açıksa, yeniden simgesini seçerek yeni bir tane yerine çalışan örneği açıldığını anlamına gelir. Uygulamanın ek örneklerini gerekiyorsa açıklandığı gibi açmak için sistem isteyebilir [sonraki bölümde](#open-a-second-instance-of-visual-studio-for-mac).

Ayrıca, bir çözümü açtığınızda, yeni bir çalışma alanında çözümü açın ve (gerekirse) geçerli çalışma kapatmak için varsayılan davranışı olan. Geçerli çalışma açıklandığı gibi açık tutarak bu varsayılan davranışı geçersiz kılabilirsiniz [ikinci bir çözüm açın](#open-a-second-solution-inside-a-single-instance) bölümü.

## <a name="open-a-second-instance-of-visual-studio-for-mac"></a>Mac için Visual Studio ikinci bir örneğini açın

Tümleşik geliştirme ortamı (IDE) ikinci bir örneğini açmak için Aç **Terminal** uygulama ve şu satırı girin:

```bash
open -n "/Applications/Visual Studio.app"
```

## <a name="open-a-second-solution-inside-a-single-instance"></a>Tek bir örnek içinde ikinci bir çözüm açın

İlk çözümünüzü birlikte ikinci bir çözümü açmak için aşağıdaki adımları kullanın:

1. İlk çözümünüzü zaten açıkken, seçin **dosya** > **açın**.
2. Varolan bir çözümü bulmak üzere dosya sisteminde göz atın.
3. Seçin **.sln** dosya ve seçin **seçenekleri**:

    ![Ekran görüntüsü, Mac için Visual Studio, .sln dosyasını ve vurgulanmış seçenekleri](media/open-multiple-solutions-image3.png)

4. NET **çalışma alanını Kapat** kutusunda:

    ![Kapat geçerli çalışma alanı kutusu ekran görüntüsü, Seçenekler iletişim kutusu işaretli](media/open-multiple-solutions-image1.png)

5. Seçin **açın** çözüm panelinde ikinci çözümü açın.

Alternatif olarak, kısa süre önce çözüm açtıysanız, aşağıdaki adımları kullanabilirsiniz:

1. Git **dosya** > **son çözümleri**.

    ![Son çözümleri menüsünün ekran görüntüsü](media/open-multiple-solutions-image2.png)

1. Basılı **Ctrl** anahtar ve çözümü seçin. Bu birleşim ikinci çözüm çözüm bölmesi açılır.

## <a name="related-video"></a>İlgili Video

> [!Video https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Visual-Studio-for-Mac-Work-With-Multiple-Solutions/player]
