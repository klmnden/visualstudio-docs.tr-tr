---
title: CaptureCurrentFrame | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4509311d-6fe2-4b65-9b4a-ff0522585d6a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c96a931593771e381d8f526919a5180da1eb919a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990168"
---
# <a name="capturecurrentframe"></a>CaptureCurrentFrame
Geçerli kare grafik günlük dosyasına geri kalanında yakalar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void CaptureCurrentFrame();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Şu anda başka bir yakalama devam ediyor durumunda — tarafından başlatılan bir yakalama gibi `BeginCapture` işlevi — söz konusu yakalama tamamlandı ve ayrı bir kare olarak grafik günlüğüne kaydedilmiş. Daha sonra farklı bir çerçeve olarak da kaydedilir geçerli çerçeve geri kalanında yakalama grafik tanılama başlar hemen. Geçerli çerçevenin son sunmak için bir çağrı tarafından işaretlenir.  
  
 Bir kareyi yakalamak için yakalama ve grafik bilgilerini kaydetmek için uygulamanızı hazırlama — diğer bir deyişle, çağrısı yapmanız gerekir [Init](init.md) örneği üzerinden `VsgDbg` çağırmadan önce sınıfı `CaptureCurrentFrame`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Init](init.md)   
 [BeginCapture](begincapture.md)