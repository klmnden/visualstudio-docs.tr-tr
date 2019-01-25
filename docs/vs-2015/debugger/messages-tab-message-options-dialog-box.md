---
title: İletiler sekmesi, ileti seçenekleri iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- message options, Messages
ms.assetid: fb9fa211-e82c-40a5-9e4b-ba8de07313c0
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a9eb1c88d935fa307e8b86a9a75da423bc08111c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54761238"
---
# <a name="messages-tab-message-options-dialog-box"></a>İletiler Sekmesi, İleti Seçenekleri İletişim Kutusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kullanım **iletileri** listesine ileti türlerini seçmek için sekmesinde [iletiler görünümünü](../debugger/messages-view.md)ve ileti arama ölçütlerini belirtmek için. Görüntülenecek [ileti seçenekleri iletişim kutusu](../debugger/message-options-dialog-box.md), seçin **günlük iletilerini** gelen **Spy** menüsü.  
  
 Genellikle, ilk kez seçtiğinizde **ileti grupları**ve seçim tek tek seçerek ince ayar yapma **görünümüne iletileri**. **Tüm** düğmesini seçer tüm ileti türleri ve **hiçbiri** düğmesi tüm türleri temizler.  
  
 Aşağıdaki ayarlar kullanılabilir **iletileri** sekmesinde:  
  
 **İletiler görünümü**  
 Belirli iletileri görüntülemek için seçin. Yeni bir ileti penceresinde oluşturduğunuzda, onu tüm iletileri görüntüleyebilirsiniz. Filtre zaman gelen iletileri **iletileri** sekmesinde, filtre yalnızca uygulandığı yeni iletileri, zaten Windows görünümünde görüntülenen iletileri.  
  
 **İleti grupları**  
 İleti gruplarını görüntülemek için seçin. Kullanılabilir gruplar şunlardır:  
  
- WM_USER: bir kod ile büyüktür veya eşittir WM_USER  
  
- Kayıtlı: kayıtlı **RegisterWindowMessage** çağırın  
  
- Bilinmiyor: Bilinmeyen iletileri 0 aralığındaki (WM_USER – 1)  
  
  Unutmayın bu **ileti grupları** altında belirli girdiler için eşlemeyin **iletiler için görünümü**. Bir grubu seçtiğinizde, doğrudan ileti akışına seçimi uygulanır.  
  
  Gri bir onay kutusu içinde **ileti grupları** belirten **iletiler için görünümü** liste kutusu, o gruptaki iletileri değiştirildi; ileti türlerini o gruptaki tüm seçilir.  
  
  **Ayarları varsayılan olarak Kaydet**  
  Daha sonra kullanmak için geçerli ayarları ileti arama seçenekleri kaydedin. Bu ayarlar, ayrıca Spy ++ çıkarken kaydedilir.
