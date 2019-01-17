---
title: İşlevi, geçerli bir prototip nesnesi yok | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5023
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b9e34652-190f-4b57-b253-df2e8c4d09c6
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a4e2cbf198a452cd61f1355682ea3041436d2a27
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346702"
---
# <a name="function-does-not-have-a-valid-prototype-object"></a>İşlevin geçerli bir prototip nesnesi yok
Kullanma girişiminde **instanceof** bir nesne belirli bir işlevi sınıfından türetilmiş ancak nesnenin yeniden belirlemek için `prototype` özelliği olarak ya da `null`, veya bir dış nesne türü (her iki geçersiz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesneleri). Bir dış nesne konak nesne modeli (örneğin, Internet Explorer'ın belge veya pencere nesnesi) bir nesneden veya dış bir COM nesnesi olabilir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   İşlevin olun `prototype` özelliği geçerli bir başvuruyor [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [prototype Özelliği (Nesne)](../../javascript/reference/prototype-property-object-javascript.md)