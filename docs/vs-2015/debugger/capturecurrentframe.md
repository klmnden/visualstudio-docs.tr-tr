---
title: CaptureCurrentFrame | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 4509311d-6fe2-4b65-9b4a-ff0522585d6a
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2718e800e2a31eb66319259ed1e43f2ab8b084c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68161639"
---
# <a name="capturecurrentframe"></a>CaptureCurrentFrame
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Geçerli kare grafik günlük dosyasına geri kalanında yakalar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void CaptureCurrentFrame();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Şu anda başka bir yakalama devam ediyor durumunda — tarafından başlatılan bir yakalama gibi `BeginCapture` işlevi — söz konusu yakalama tamamlandı ve ayrı bir kare olarak grafik günlüğüne kaydedilmiş. Daha sonra farklı bir çerçeve olarak da kaydedilir geçerli çerçeve geri kalanında yakalama grafik tanılama başlar hemen. Geçerli çerçevenin son sunmak için bir çağrı tarafından işaretlenir.  
  
 Bir kareyi yakalamak için yakalama ve grafik bilgilerini kaydetmek için uygulamanızı hazırlama — diğer bir deyişle, çağrısı yapmanız gerekir [Init](../debugger/init.md) örneği üzerinden `VsgDbg` çağırmadan önce sınıfı `CaptureCurrentFrame`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Init](../debugger/init.md)   
 [BeginCapture](../debugger/begincapture.md)
