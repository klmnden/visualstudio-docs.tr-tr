---
title: VBArray bekleniyor | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5013
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: f2998d7d-13a4-4bbe-b872-3ff3316551e4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 159a5dd0195cc0cbb244664d75e19d1ac6af3dec
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56843422"
---
# <a name="vbarray-expected"></a>VBArray bekleniyor
Temin ettiğiniz beklenen bir Visual Basic SAFEARRAY'i değil bir nesne.  
  
```js
new VBArray(safeArray);  
```  
  
 VBArrays salt okunurdur ve doğrudan oluşturulamıyor. SafeArray bağımsız değişkeni bir VBArray değerdir ve VBArray değeri için iletilmeden önce almış olmanız gerekir `VBArray` Oluşturucusu. Bu, varolan bir ActiveX veya başka nesneden değeri alarak yalnızca yapılabilir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yalnızca geçirdiğiniz olun **VBArray** nesneleri için **VBArray** Oluşturucusu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VBArray nesnesi](../../javascript/reference/vbarray-object-javascript.md)   
 [Dizileri Kullanma](../../javascript/advanced/using-arrays-javascript.md)