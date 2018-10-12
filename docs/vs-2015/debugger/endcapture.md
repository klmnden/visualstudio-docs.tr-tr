---
title: EndCapture | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 06084c3b-e065-49b6-968e-d578762fb871
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8655d2f99a9d69319b6019fdec6ad2fcdbbedbeb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49182838"
---
# <a name="endcapture"></a>EndCapture
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İle başlatılan bir yakalama zaman aralığı sona `BeginCapture`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void EndCapture();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bir yakalama aralığı genellikle bir alt kümesini çizim çağrısı belirli bir tür hakkında yalnızca grafik bilgisi yakalamak istediğinizde gibi bir çerçeve yayılır. Ardından yakalama aralığı sunmak için bir çağrı yayılırsa, grafik bilgilerini iki çerçeve yakalanır. İlk çerçeve çağrı aralığını kapsayan `BeginCapture` ve sunmak için; çağrı ikinci çerçevesi sunmak için çağrısından sonra ilk Direct3D olay çağrısı arasındaki aralık yayılan `EndCapture`.  
  
 Bir aralık yakalamak için grafik bilgilerini yakalama ve kaydetmeye uygulamanızı hazırlama — diğer bir deyişle, çağrısı yapmanız gerekir [Init](../debugger/init.md) örneği üzerinden `VsgDbg` çağırmadan önce sınıfı `BeginCapture` veya `EndCapture`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [BeginCapture](../debugger/begincapture.md)   
 [CaptureCurrentFrame](../debugger/capturecurrentframe.md)



