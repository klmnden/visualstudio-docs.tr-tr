---
title: Beklenen ']' (JavaScript) normal ifadede | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5019
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 1ca2079a-44dd-479f-a1e3-e04a14d0739e
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 66fa8ba2396185bd402e4bc31a3da6b1f8bf95ab
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446489"
---
# <a name="expected--in-regular-expression-javascript"></a>Normal ifadede ']' bekleniyor (JavaScript)
Bir karakter sınıfı için bir normal ifade eşleştirmesi oluşturulmaya çalışıldı, ancak sağ köşeli ayraç içermiyordu. Köşeli ayraçlar yerleştirerek tek değişmez bir karakter birleşimleri karakter sınıflara birleştirilebilecek. Bir karakter sınıfı, içerdiği herhangi bir karakterle eşleşir. Örneğin, / [abc] / "a", "b", herhangi bir harf ile eşleşir veya "c".  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Normal ifade sağ köşeli ayraç ekleyin.  
  
    > [!NOTE]
    > Ters eğik çizgi ile - tek bir köşeli ayraç eşleştirmek istiyorsanız, atlatmak \\[- özel bir karakter olarak yorumlanmaz şekilde [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)].  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Normal ifade nesnesi](../../javascript/reference/regular-expression-object-javascript.md)   
 [Normal ifade söz dizimi (JavaScript)](https://msdn.microsoft.com/library/1400241x)