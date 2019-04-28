---
title: Kodlanacak URI geçersiz karakter içeriyor. | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5024
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: a3f0fdbb-8d4b-41ae-a396-43dfc9483760
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f2f9111acf656bf882a3d506fe95b8361f3693ff
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63006214"
---
# <a name="the-uri-to-be-encoded-contains-an-invalid-character"></a>Kodlanacak URI geçersiz karakter içeriyor
Bir dize URI'si (Tekdüzen Kaynak Tanımlayıcısı) kodlamak çalıştı, ancak geçersiz karakterler içeriyor. Çoğu karakter için bir URI'leri dönüştürülecek dize içinde geçerli olsa da, bazı Unicode karakter dizileri geçersizdir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Kodlanacak dize yalnızca geçerli Unicode dizileri içeren emin olun. Tam bir URI bileşenlerini ayırıcıları ve bir dizi oluşur. Açılı ayraçlar adlarında bileşenleri temsil eder ve ":", "/", ";" ve "?" ayırıcı olarak kullanılan ayrılmış karakterler. Genel formu şöyledir:  
  
    ```JavaScript  
    <Scheme>:<first>/<second>;<third>?<fourth>  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [encodeURI işlevi](../../javascript/reference/encodeuri-function-javascript.md)   
 [encodeURIComponent İşlevi](../../javascript/reference/encodeuricomponent-function-javascript.md)