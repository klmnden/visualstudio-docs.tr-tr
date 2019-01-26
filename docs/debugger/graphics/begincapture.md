---
title: BeginCapture | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 9edbb52d-ee0b-4cc4-a382-972bcee067d3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 536fac55c68a7736a37961ccab2741d6b8aedd41
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54993188"
---
# <a name="begincapture"></a>BeginCapture
İle biten bir yakalama aralık başlar `EndCapture`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void BeginCapture();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bir yakalama aralığı genellikle bir alt kümesini çizim çağrısı belirli bir tür hakkında yalnızca grafik bilgisi yakalamak istediğinizde gibi bir çerçeve yayılır. Ardından yakalama aralığı sunmak için bir çağrı yayılırsa, grafik bilgilerini iki çerçeve yakalanır. İlk çerçeve çağrı aralığını kapsayan `BeginCapture` ve sunmak için; çağrı ikinci çerçevesi sunmak için çağrısından sonra ilk Direct3D olay çağrısı arasındaki aralık yayılan `EndCapture`.  
  
 Bir aralık yakalamak için grafik bilgilerini yakalama ve kaydetmeye uygulamanızı hazırlama — diğer bir deyişle, çağrısı yapmanız gerekir [Init](init.md) örneği üzerinden `VsgDbg` çağırmadan önce sınıfı `BeginCapture` veya `EndCapture`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [EndCapture](endcapture.md)   
 [CaptureCurrentFrame](capturecurrentframe.md)