---
title: Dizi uzunluğu sonlu pozitif bir tamsayı olması gerekir | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5029
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 1a467040-4702-4178-848f-418a5974e907
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 31673205a7ca94783985e0249c5664b4bbca6147
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62818130"
---
# <a name="array-length-must-be-a-finite-positive-integer"></a>Dizi uzunluğu sonlu pozitif bir tamsayı olmalıdır
Aradığınız **dizi** Oluşturucu ile bağımsız değişken (tam sayılara oluşur sıfır ve pozitif tam sayılar kümesini oluşan) bir tamsayı değil.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Pozitif tam sayılar yalnızca yeni bir oluştururken kullanacağınız `Array` nesne. Bir tamsayı değil tek bir öğe ile bir dizi oluşturmak istiyorsanız, bunu bir işlemdir. Önce bir dizi olan bir öğe oluşturun, sonra içindeki ilk öğeye (array[0]). değer yerleştirin Bu hatayı oluşturan bir örnek verilmiştir.  
  
    ```JavaScript  
    var piArray = new Array(3.14159);  
    ```  
  
     Aşağıdaki örnek, bir dizi sayısal tek bir öğe belirtmek için doğru şekilde gösterir.  
  
    ```JavaScript  
    var piArray = new Array(1);  
    piArray [0] = 3.14159;  
    ```  
  
     En büyük tamsayı değer (yaklaşık 4 milyarı aşan) dışında bir dizinin boyutu için üst sınır yoktur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dizileri Kullanma](../../javascript/advanced/using-arrays-javascript.md)