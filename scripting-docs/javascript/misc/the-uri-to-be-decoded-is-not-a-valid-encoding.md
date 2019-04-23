---
title: Kodu çözülecek URI geçerli bir kodlamada değil | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5025
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 029e0790-ffd1-496d-8700-3b3dbac1b6fd
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8fd8add72d016bc3f2e815f41c29c735505c8817
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60108431"
---
# <a name="the-uri-to-be-decoded-is-not-a-valid-encoding"></a>Kodu çözülecek URI geçerli bir kodlamada değil
Düzensiz biçimlendirilmiş bir URI (Tekdüzen Kaynak Tanımlayıcısı) kod çözme çalışıldı. URI, özel bir sözdizimi vardır; bir URI ile kullanılabilmesi için çoğu alfasayısal olmayan karakter kodlanmış olması gerekir. Kullanabileceğiniz `encodeURI` ve `encodeURIComponent` bir normal bir URI oluşturmak için yöntemleri [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] dize.  
  
 Tam bir URI bileşenlerini ayırıcıları ve bir dizi oluşur. Genel formu şöyledir:  
  
```JavaScript  
<Scheme>:<first>/<second>;<third>?<fourth>  
```  
  
 Açılı ayraçlar adlarında bileşenleri temsil eder ve ":", "/", ";" ve "?" ayırıcı olarak kullanılan ayrılmış karakterler.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Geçerli bir URI'leri çözmeye çalıştığınız emin olun. Normal çözülemiyor [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] dizeleri gibi geçersiz karakterler içeriyor olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [decodeURI işlevi](../../javascript/reference/decodeuri-function-javascript.md)   
 [decodeURIComponent İşlevi](../../javascript/reference/decodeuricomponent-function-javascript.md)