---
title: Beklenen onaltılık basamak | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT1023
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 67a86df7-49f9-43cb-99c6-99b1a427827a
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2c2507acd42336511dadc3dedd2eba15fe0d5b76
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60050081"
---
# <a name="expected-hexadecimal-digit"></a>Beklenen onaltılık basamak
Yanlış bir Unicode kaçış dizisi oluşturduğunuz. Unicode kaçış dizileri \u, tam olarak dört onaltılık basamağın (daha fazla ve en az) geldiği başlar. Unicode onaltılık basamak yalnızca sayı 0-9, A-F büyük harf ve küçük harf a-f içerebilir. Aşağıdaki örnek, doğru biçimlendirilmiş bir Unicode çıkış dizisi gösterir.  
  
```JavaScript  
z = "\u1A5F";  
```  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Unicode onaltılık basamak \u ile başlamak için yalnızca 0-9, A-F, küçük harf a-f büyük harf sayıları içeren emin olun; ve dört basamak gruplandırılır.  
  
    > [!NOTE]
    >  Bir dizede metin \u kullanın, ardından iki ters eğik çizgi - kullanmak istiyorsanız (\\\u)-ilk ters eğik çizgi kaçış için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Veri Türleri](../../javascript/data-types-javascript.md)