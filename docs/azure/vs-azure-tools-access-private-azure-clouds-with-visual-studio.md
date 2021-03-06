---
title: Azure özel bulutlara erişme
description: Visual Studio kullanarak özel bulut kaynakları erişmeyi öğrenin.
author: ghogen
manager: jillfra
assetId: 9d733c8d-703b-44e7-a210-bb75874c45c8
ms.custom: seodec18
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 11/13/2017
ms.author: ghogen
ms.openlocfilehash: 5f9ea7ac26742b0fc1c116dfe53e941f93358221
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62551210"
---
# <a name="accessing-private-azure-clouds-with-visual-studio"></a>Visual Studio ile Azure özel bulutlara erişme

Varsayılan olarak, Visual Studio, Azure bulut REST uç noktalarını destekler. Bu makalede, özel bulutunuzun sertifika erişmek ve Visual Studio'dan bir özel bulutla etkileşim kurmak için nasıl kullanılacağını öğrenin.

1. Özel bulut için Azure portalında, yayımlama ayarları dosyasını indirin veya bir yayımlama ayarları dosyası için yöneticinize başvurun. (Dosya uzantısına sahip `.publishsettings`.)

1. Visual Studio'da **Sunucu Gezgini**, sağ **Azure** düğümünü seçip alt **yönetin ve filtre abonelikleri**.

    ![Komut Abonelikleri Yönetme](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790778.png)

1. İçinde **Microsoft Azure abonelikleri yönetme** iletişim kutusunda **sertifikaları** sekmesine ve ardından seçin **alma**.

    ![Azure sertifikaları içeri aktarma](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790779.png)

1. İçinde **alma Microsoft Azure abonelikleri** iletişim kutusunda **Gözat**.

    ![Gözat düğmesi alma Microsoft Azure abonelikleri iletişim](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/browse-button.png)

1. İçinde **açık** Seç dosyasını ve ardından seçin iletişim kutusu, yayımlama ayarları dosyasını kaydettiğiniz dizine gidin **açık**.

    ![Yayımlama ayarları dosyası seçin](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/select-publish-settings-file.png)

1. İçin döndürülen **alma Microsoft Azure abonelikleri** iletişim kutusunda **alma**.

    ![Yayımlama ayarları dosyasını içeri aktar](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790780.png)

    Sertifikaları yayımlama ayarlarını dosyasından Visual Studio'ya içeri aktarılır ve artık, özel bulut kaynakları ile etkileşim kurabilir.
