---
title: DEBUG_TEXT sabitleri | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 5dde10c3-7040-46b1-a328-959c6ce5cd9f
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2342555c4ee92b403aa01cc0ca15bb805f2b002e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152804"
---
# <a name="debugtext-constants"></a>DEBUG_TEXT Sabitleri
Sırasında kullanılan [Idebugexpressioncontext::parselanguagetext](../../winscript/reference/idebugexpressioncontext-parselanguagetext.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef DWORD DEBUG_TEXT;  
```  
  
## <a name="constants"></a>Sabitler  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|DWORD DEBUG_TEXT_ISEXPRESSION|0x00000001|Metin bir ifadenin bir deyim aksine olduğunu gösterir. Bu bayrak, metin bazı diller tarafından ayrıştırılır şekilde etkileyebilir.|  
|DEBUG_TEXT_RETURNVALUE|0x00000002|Dönüş değeri varsa, çağıran tarafından kullanılır.|  
|DEBUG_TEXT_NOSIDEEFFECTS|0x00000004|Yan etkileri izin vermez. İfadenin değerlendirilmesi, bu bayrağı ayarlarsanız, hiçbir çalışma zamanı durumu değiştirmeniz gerekir.|  
|DEBUG_TEXT_ALLOWBREAKPOINTS|0x00000008|Metin değerlendirmesi sırasında kesme noktaları sağlar. Bu bayrak ayarlanmazsa, metin değerlendirmesi sırasında kesme noktaları yoksayılacak.|  
|DEBUG_TEXT_ALLOWERRORREPORT|0x00000010|Hata raporları, metin değerlendirmesi sırasında izin verir. Bu bayrak ayarlanmazsa, ardından hataları konağa değerlendirmesi sırasında raporlanmayacaktır.|  
|DEBUG_TEXT_EVALUATETOCODECONTEXT|0x00000020|Deyimi çalıştırmak yerine bir kod içeriği için değerlendirilecek ifade olduğunu gösterir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)