---
title: Beklenen ']' (JavaScript) normal ifadede | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT5019
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 1ca2079a-44dd-479f-a1e3-e04a14d0739e
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e0b34ae4bdf04d261647b9096cda13eec75617c5
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349432"
---
# <a name="expected--in-regular-expression-javascript"></a>Normal ifadede ']' bekleniyor (JavaScript)
Bir karakter sınıfı için bir normal ifade eşleştirmesi oluşturulmaya çalışıldı, ancak sağ köşeli ayraç içermiyordu. Köşeli ayraçlar yerleştirerek tek değişmez bir karakter birleşimleri karakter sınıflara birleştirilebilecek. Bir karakter sınıfı, içerdiği herhangi bir karakterle eşleşir. Örneğin, / [abc] / "a", "b", herhangi bir harf ile eşleşir veya "c".  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Normal ifade sağ köşeli ayraç ekleyin.  
  
    > [!NOTE]
    >  Ters eğik çizgi ile - tek bir köşeli ayraç eşleştirmek istiyorsanız, atlatmak \\[- özel bir karakter olarak yorumlanmaz şekilde [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)].  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Normal ifade nesnesi](../../javascript/reference/regular-expression-object-javascript.md)   
 [Normal ifade söz dizimi (JavaScript)](https://msdn.microsoft.com/library/1400241x)