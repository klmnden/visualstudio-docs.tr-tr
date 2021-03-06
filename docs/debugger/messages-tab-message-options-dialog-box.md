---
title: İletiler sekmesi, ileti seçenekleri iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- message options, Messages
ms.assetid: fb9fa211-e82c-40a5-9e4b-ba8de07313c0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: de50e6fe997ce10266cbb51f2fd91c318ab2bd1f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62905538"
---
# <a name="messages-tab-message-options-dialog-box"></a>İletiler Sekmesi, İleti Seçenekleri İletişim Kutusu
Kullanım **iletileri** listesine ileti türlerini seçmek için sekmesinde [iletiler görünümünü](../debugger/messages-view.md)ve ileti arama ölçütlerini belirtmek için. Görüntülenecek [ileti seçenekleri iletişim kutusu](../debugger/message-options-dialog-box.md), seçin **günlük iletilerini** gelen **Spy** menüsü.

 Genellikle, ilk kez seçtiğinizde **ileti grupları**ve seçim tek tek seçerek ince ayar yapma **görünümüne iletileri**. **Tüm** düğmesini seçer tüm ileti türleri ve **hiçbiri** düğmesi tüm türleri temizler.

 Aşağıdaki ayarlar kullanılabilir **iletileri** sekmesinde:

 **İletiler görünümü** belirli iletileri görüntülemek için seçin. Yeni bir ileti penceresinde oluşturduğunuzda, onu tüm iletileri görüntüleyebilirsiniz. Filtre zaman gelen iletileri **iletileri** sekmesinde, filtre yalnızca uygulandığı yeni iletileri, zaten Windows görünümünde görüntülenen iletileri.

 **İleti grupları** görüntülemek için ileti grupları seçin. Kullanılabilir gruplar şunlardır:

- WM_USER: bir kod ile büyüktür veya eşittir WM_USER

- Kayıtlı: kayıtlı **RegisterWindowMessage** çağırın

- Bilinmiyor: Bilinmeyen iletileri 0 aralığındaki (WM_USER - 1)

  Unutmayın bu **ileti grupları** altında belirli girdiler için eşlemeyin **iletiler için görünümü**. Bir grubu seçtiğinizde, doğrudan ileti akışına seçimi uygulanır.

  Gri bir onay kutusu içinde **ileti grupları** belirten **iletiler için görünümü** liste kutusu, o gruptaki iletileri değiştirildi; ileti türlerini o gruptaki tüm seçilir.

  **Ayarları varsayılan olarak Kaydet** ileti arama seçenekleri daha sonra kullanmak için geçerli ayarları kaydedin. Bu ayarlar, ayrıca Spy ++ çıkarken kaydedilir.