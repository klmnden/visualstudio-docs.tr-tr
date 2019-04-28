---
title: İşlevi, geçerli bir prototip nesnesi yok | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5023
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b9e34652-190f-4b57-b253-df2e8c4d09c6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 413f73a53a6d4f698219139a87c449be4c155831
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63007509"
---
# <a name="function-does-not-have-a-valid-prototype-object"></a>İşlevin geçerli bir prototip nesnesi yok
Kullanma girişiminde **instanceof** bir nesne belirli bir işlevi sınıfından türetilmiş ancak nesnenin yeniden belirlemek için `prototype` özelliği olarak ya da `null`, veya bir dış nesne türü (her iki geçersiz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesneleri). Bir dış nesne konak nesne modeli (örneğin, Internet Explorer'ın belge veya pencere nesnesi) bir nesneden veya dış bir COM nesnesi olabilir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- İşlevin olun `prototype` özelliği geçerli bir başvuruyor [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [prototype Özelliği (Nesne)](../../javascript/reference/prototype-property-object-javascript.md)