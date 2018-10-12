---
title: BeginCapture | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9edbb52d-ee0b-4cc4-a382-972bcee067d3
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c8580283e19b61356746ecca8a707369abc45355
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49299305"
---
# <a name="begincapture"></a>BeginCapture
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İle biten bir yakalama aralık başlar `EndCapture`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void BeginCapture();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Bir yakalama aralığı genellikle bir alt kümesini çizim çağrısı belirli bir tür hakkında yalnızca grafik bilgisi yakalamak istediğinizde gibi bir çerçeve yayılır. Ardından yakalama aralığı sunmak için bir çağrı yayılırsa, grafik bilgilerini iki çerçeve yakalanır. İlk çerçeve çağrı aralığını kapsayan `BeginCapture` ve sunmak için; çağrı ikinci çerçevesi sunmak için çağrısından sonra ilk Direct3D olay çağrısı arasındaki aralık yayılan `EndCapture`.  
  
 Bir aralık yakalamak için grafik bilgilerini yakalama ve kaydetmeye uygulamanızı hazırlama — diğer bir deyişle, çağrısı yapmanız gerekir [Init](../debugger/init.md) örneği üzerinden `VsgDbg` çağırmadan önce sınıfı `BeginCapture` veya `EndCapture`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [EndCapture](../debugger/endcapture.md)   
 [CaptureCurrentFrame](../debugger/capturecurrentframe.md)



