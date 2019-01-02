---
title: İletiler sekmesi, ileti seçenekleri iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- message options, Messages
ms.assetid: fb9fa211-e82c-40a5-9e4b-ba8de07313c0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1f7675039f8e5f5fb5c1d5899b96682ab60a2bc0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53830605"
---
# <a name="messages-tab-message-options-dialog-box"></a>İletiler Sekmesi, İleti Seçenekleri İletişim Kutusu
Kullanım **iletileri** listesine ileti türlerini seçmek için sekmesinde [iletiler görünümünü](../debugger/messages-view.md)ve ileti arama ölçütlerini belirtmek için. Görüntülenecek [ileti seçenekleri iletişim kutusu](../debugger/message-options-dialog-box.md), seçin **günlük iletilerini** gelen **Spy** menüsü.  
  
 Genellikle, ilk kez seçtiğinizde **ileti grupları**ve seçim tek tek seçerek ince ayar yapma **görünümüne iletileri**. **Tüm** düğmesini seçer tüm ileti türleri ve **hiçbiri** düğmesi tüm türleri temizler.  
  
 Aşağıdaki ayarlar kullanılabilir **iletileri** sekmesinde:  
  
 **İletiler görünümü**  
 Belirli iletileri görüntülemek için seçin. Yeni bir ileti penceresinde oluşturduğunuzda, onu tüm iletileri görüntüleyebilirsiniz. Filtre zaman gelen iletileri **iletileri** sekmesinde, filtre yalnızca uygulandığı yeni iletileri, zaten Windows görünümünde görüntülenen iletileri.  
  
 **İleti grupları**  
 İleti gruplarını görüntülemek için seçin. Kullanılabilir gruplar şunlardır:  
  
- WM_USER: bir kod ile büyüktür veya eşittir WM_USER  
  
- Kayıtlı: kayıtlı **RegisterWindowMessage** çağırın  
  
- Bilinmiyor: Bilinmeyen iletileri 0 aralığındaki (WM_USER - 1)  
  
  Unutmayın bu **ileti grupları** altında belirli girdiler için eşlemeyin **iletiler için görünümü**. Bir grubu seçtiğinizde, doğrudan ileti akışına seçimi uygulanır.  
  
  Gri bir onay kutusu içinde **ileti grupları** belirten **iletiler için görünümü** liste kutusu, o gruptaki iletileri değiştirildi; ileti türlerini o gruptaki tüm seçilir.  
  
  **Ayarları varsayılan olarak Kaydet**  
  Daha sonra kullanmak için geçerli ayarları ileti arama seçenekleri kaydedin. Bu ayarlar, ayrıca Spy ++ çıkarken kaydedilir.