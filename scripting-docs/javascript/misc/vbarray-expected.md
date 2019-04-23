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
ms.openlocfilehash: 5d1fabd8da6f825a266614a4a5c7fabd5c307130
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60064953"
---
# <a name="vbarray-expected"></a>VBArray bekleniyor
Temin ettiğiniz beklenen bir Visual Basic SAFEARRAY'i değil bir nesne.  
  
```js
new VBArray(safeArray);  
```  
  
 VBArrays salt okunurdur ve doğrudan oluşturulamıyor. SafeArray bağımsız değişkeni bir VBArray değerdir ve VBArray değeri için iletilmeden önce almış olmanız gerekir `VBArray` Oluşturucusu. Bu, varolan bir ActiveX veya başka nesneden değeri alarak yalnızca yapılabilir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Yalnızca geçirdiğiniz olun **VBArray** nesneleri için **VBArray** Oluşturucusu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VBArray nesnesi](../../javascript/reference/vbarray-object-javascript.md)   
 [Dizileri Kullanma](../../javascript/advanced/using-arrays-javascript.md)