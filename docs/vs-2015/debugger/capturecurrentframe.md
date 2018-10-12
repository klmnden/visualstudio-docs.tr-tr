---
title: CaptureCurrentFrame | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4509311d-6fe2-4b65-9b4a-ff0522585d6a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b33cad0ad67d874ff5595eac7b634cc9810257f2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49190703"
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



