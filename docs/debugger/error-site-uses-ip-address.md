---
title: 'Hata: Sitesinin kullandığı IP adresi | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.webdbg_siteusesipaddress
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d8aa34553f4fb6d4524357f830dbbeabe3296354
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54981122"
---
# <a name="error-site-uses-ip-address"></a>Hata: Site IP adresi kullanıyor
Hata ayıklayıcı bir IP adresi kullanarak bir Web uygulaması için otomatik iliştirme çalıştığında bu hata oluşur. Değiştirirseniz böyle **Web sitesi kimliği** için **belirli IP adreslerini kullanan** IIS'de.  
  
 İçin otomatik çalışmaya iliştirme, projeyi yalnızca makine adı yerine belirli bir IP adresi ile oluşturmanız gerekir. Aksi takdirde, hata ayıklayıcı makine adı için IIS debug fiilini göndermek bir hata neden olacak localhost değişecektir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Kullanım el ile eklemek yerine (hata ayıklama menüsünden **iliştirme**).  
  
     —veya—  
  
2.  Değişiklik **IIS Web sitesi kimliği** ayarı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)