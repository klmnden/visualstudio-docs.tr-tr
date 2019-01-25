---
title: 'Hata: Sitesinin kullandığı IP adresi | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.webdbg_siteusesipaddress
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: b2b8ddc8-746d-46e3-87a6-b956b1ee048d
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e040c45079c9e4b82337cbd1e4b5d7d8306e1a32
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54761216"
---
# <a name="error-site-uses-ip-address"></a>Hata: Site IP adresi kullanıyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata ayıklayıcı bir IP adresi kullanarak bir Web uygulaması için otomatik iliştirme çalıştığında bu hata oluşur. Değiştirirseniz böyle **Web sitesi kimliği** için **belirli IP adreslerini kullanan** IIS'de.  
  
 İçin otomatik çalışmaya iliştirme, projeyi yalnızca makine adı yerine belirli bir IP adresi ile oluşturmanız gerekir. Aksi takdirde, hata ayıklayıcı makine adı için IIS debug fiilini göndermek bir hata neden olacak localhost değişecektir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Kullanım el ile eklemek yerine (hata ayıklama menüsünden **iliştirme**).  
  
     —veya—  
  
2.  Değişiklik **IIS Web sitesi kimliği** ayarı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)
