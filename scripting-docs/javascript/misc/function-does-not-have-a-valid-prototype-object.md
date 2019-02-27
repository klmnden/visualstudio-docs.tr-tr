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
ms.openlocfilehash: 31226f972ff4714dd81207cf27d862d3449184a5
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56840769"
---
# <a name="function-does-not-have-a-valid-prototype-object"></a>İşlevin geçerli bir prototip nesnesi yok
Kullanma girişiminde **instanceof** bir nesne belirli bir işlevi sınıfından türetilmiş ancak nesnenin yeniden belirlemek için `prototype` özelliği olarak ya da `null`, veya bir dış nesne türü (her iki geçersiz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesneleri). Bir dış nesne konak nesne modeli (örneğin, Internet Explorer'ın belge veya pencere nesnesi) bir nesneden veya dış bir COM nesnesi olabilir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   İşlevin olun `prototype` özelliği geçerli bir başvuruyor [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlev nesnesi](../../javascript/reference/function-object-javascript.md)   
 [prototype Özelliği (Nesne)](../../javascript/reference/prototype-property-object-javascript.md)