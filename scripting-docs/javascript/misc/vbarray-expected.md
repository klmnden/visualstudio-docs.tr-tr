---
title: VBArray bekleniyor | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5013
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: f2998d7d-13a4-4bbe-b872-3ff3316551e4
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a4b5416c6e37e59a60206bd21606b5214f05a269
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347469"
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