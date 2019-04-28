---
title: Dizi uzunluğu sonlu pozitif bir sayı atanmalıdır | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5030
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: c51c66a4-a543-4e95-b18d-2cfbcb3d1fdd
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 39f2720efbcd8defffb9d0c77047a50e57939e95
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62818060"
---
# <a name="array-length-must-be-assigned-a-finite-positive-number"></a>Dizi uzunluğuna sonsuz olmayan pozitif bir sayı atanmalıdır
Ayarlarken **uzunluğu** , varolan bir özellik **dizi** nesnesi, pozitif bir sayı veya sıfır olmayan bir dizi uzunluğu belirtildi. Bir değer atadığınızda, bu hata oluşur **uzunluğu** özelliği bir `Array` negatif nesnesini veya sayı olmayan (`NaN`). Unutmayın [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] kesirli sayılar tüm tamsayılar için otomatik olarak dönüştürür.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Pozitif bir tam sayı uzunluk özelliğine atayın. En büyük tamsayı değer (yaklaşık 4 milyarı aşan) dışında bir dizinin boyutu için üst sınır yoktur. Aşağıdaki örnek, ayarlamak için doğru şekilde gösterir. **uzunluğu** özelliği bir **dizi** nesne.  
  
    ```JavaScript  
    var my_array = new Array();  
    my_array.length = 99;  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dizileri Kullanma](../../javascript/advanced/using-arrays-javascript.md)