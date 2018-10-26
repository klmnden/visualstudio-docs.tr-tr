---
title: Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi. | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.remote.dcom_access_denied
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
helpviewer_keywords:
- remote debugging, DCOM error
- remote DCOM access denied error
- DCOM, access errors
ms.assetid: 9d7dfc1b-9fe0-4f54-9c50-9c0e0f8358c5
caps.latest.revision: 30
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6fa7aca2b86e8cc7c8d9cea4eba27b850d26bc13
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49825672"
---
# <a name="a-dcom-error-occurred-trying-to-contact-the-remote-computer-access-is-denied"></a>Uzak bilgisayara erişilmeye çalışılırken DCOM hatası oluştu. Erişim reddedildi.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uzaktan hata ayıklama, aşağıdaki durumlarda yerel ve uzak bilgisayarlar arasında iletişim kurmak için DCOM kullanır:  
  
- Hata ayıklayıcı kümesine **yerel uyumluluk modu** veya **yönetilen uyumluluk modu** iade **Araçlar / Seçenekler / hata ayıklama** sayfası  
  
- Yönetilen C++ hata ayıklama (C + +/ CLI) kodu.  
  
- Visual Studio 2013'te zaman **yerel Düzenle ve Devam Et'i etkinleştir** iade **Araçlar / Seçenekler / hata ayıklama** sayfası  
  
- Bazı üçüncü taraf hata ayıklama senaryoları  
  
  Visual Studio işlemini kendi kimlik doğrulaması yapamaz (veya sağlanan kimlik bilgilerinin yeterli kabul zaman) Bu hata oluşur. DCOM üzerinden uzaktan hata ayıklayıcı işleme. Bir veya daha fazla aşağıdaki geçici çözümlerden sorunu çözebilir:  
  
- Devre dışı **yerel uyumluluk modu** ve **yönetilen uyumluluk modu**.  
  
- Visual Studio 2013'te kapatmak **yerel Düzenle ve Devam Et'i etkinleştir**.  
  
- Her iki bilgisayar yeniden başlatın.  
  
- Uzaktan hata ayıklama kimlik bilgilerinin girilmesi gerekir, kimlik bilgilerini kaydetme seçeneğini denetleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)



