---
title: Koşullu derleme kapalı | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT1030
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 59a030b0-a6c6-47f2-b90e-c0ed204d5116
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bcbf844ced2bb74ddfea9bd62d68877b7a3c969c
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347352"
---
# <a name="conditional-compilation-is-turned-off"></a>Koşullu derleme kapalı
Üzerinde koşullu derleme değişken ilk açma koşullu derleme olmadan kullanma girişimi. Üzerinde koşullu derleme bildirir [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] derleyici ile @ koşullu derleme değişkenleri olarak başlayan tanımlayıcılar yorumlamak için. Koşullu kodunuzu ifadesiyle başlayarak yapın:  
  
```js
/*@cc_on @*/  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Aşağıdaki deyim, koşullu kodunuzu başlangıcına ekleyin:  
  
    ```JavaScript  
    /*@cc_on @*/  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Koşullu derleme](../../javascript/advanced/conditional-compilation-javascript.md)   
 [Koşullu derleme değişkenleri](../../javascript/advanced/conditional-compilation-variables-javascript.md)   
 [@cc_on Deyimi](../../javascript/reference/at-cc-on-statement-javascript.md)   
 [@if Deyimi](../../javascript/reference/at-if-statement-javascript.md)   
 [@set Deyimi](../../javascript/reference/at-set-statement-javascript.md)