---
title: Kesir basamakları sayısı aralık dışında olduğundan | Microsoft Docs
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
- VS.WebClient.Help.SCRIPT5026
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: dbe05d7d-fcf6-4823-9c61-4b814d1ad3c4
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 17ffec5e6b4cfff85b49f61e7105ca8ce3d75c78
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348470"
---
# <a name="the-number-of-fractional-digits-is-out-of-range"></a>Kesir basamakları sayısı aralık dışı
Geçersiz bağımsız değişken işlevine geçirebileceğimiz çalışıldı **Number.prototype.toExponential**. İşlevin bağımsız değişkeninin **toExponential()** 0 ile 20 (sınırlar dahil) arasında olmalıdır.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Bağımsız değişkeni sağlamak **toExponential()** çok büyük veya çok küçük değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [toExponential Metodu (Sayı)](../../javascript/reference/toexponential-method-number-javascript.md)