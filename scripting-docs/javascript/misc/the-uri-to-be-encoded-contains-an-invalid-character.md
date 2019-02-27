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
ms.openlocfilehash: a3c71b90d0711bf317d0ed72d51c0d5d45297c80
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56841876"
---
# <a name="the-uri-to-be-encoded-contains-an-invalid-character"></a>Kodlanacak URI geçersiz karakter içeriyor
Bir dize URI'si (Tekdüzen Kaynak Tanımlayıcısı) kodlamak çalıştı, ancak geçersiz karakterler içeriyor. Çoğu karakter için bir URI'leri dönüştürülecek dize içinde geçerli olsa da, bazı Unicode karakter dizileri geçersizdir.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Kodlanacak dize yalnızca geçerli Unicode dizileri içeren emin olun. Tam bir URI bileşenlerini ayırıcıları ve bir dizi oluşur. Açılı ayraçlar adlarında bileşenleri temsil eder ve ":", "/", ";" ve "?" ayırıcı olarak kullanılan ayrılmış karakterler. Genel formu şöyledir:  
  
    ```JavaScript  
    <Scheme>:<first>/<second>;<third>?<fourth>  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [encodeURI işlevi](../../javascript/reference/encodeuri-function-javascript.md)   
 [encodeURIComponent İşlevi](../../javascript/reference/encodeuricomponent-function-javascript.md)