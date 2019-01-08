---
title: Döngü dışında 'break' olamaz | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT1019
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 11d02172-2a78-4705-a730-d21111db5f42
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 53f32da997b775e01959df5abc7e72fb55c1b194
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086703"
---
# <a name="cant-have-break-outside-of-loop"></a>Döngü dışında 'break' olamaz
Kullanmaya çalıştığınız **sonu** anahtar sözcüğü bir döngü dışında. **Sonu** anahtar sözcüğü, bir döngü sonlandırmak için kullanılır veya `switch` deyimi. Döngü gövdesinde gömülü olması gerekir veya `switch` deyimi. Ancak, bir **etiket** break anahtar sözcüğü izleyebilirsiniz.  
  
```js
break labelname;  
```  
  
 Yalnızca etiketli biçiminde ihtiyacınız **sonu** kullanırken anahtar sözcüğü iç içe döngüleri veya `switch` deyimlerini ve en içtekiyle olmayan bir döngüden gerek.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Emin **sonu** anahtar sözcüğü, kapsayan bir döngü veya switch deyimi içinde görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [break deyimi](../../javascript/reference/break-statement-javascript.md)   
 [Program akışı denetimi](../../javascript/controlling-program-flow-javascript.md)   
 [Komut Dosyalarınızda Sorun Giderme](../../javascript/advanced/troubleshooting-your-scripts-javascript.md)