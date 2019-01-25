---
title: '&lt;Özet&gt; (JavaScript) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- summary JavaScript XML tag
- <summary> JavaScript XML tag
ms.assetid: 6540582d-bdb3-42ec-ad2f-c176783e6f9c
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 81d41918d61bbe95cfe19d2382535449a47deb8c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54775820"
---
# <a name="ltsummarygt-javascript"></a>&lt;Özet&gt; (JavaScript)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir işlev veya metot için açıklamayı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<summary locid="descriptionID">description  
</summary>  
```  
  
#### <a name="parameters"></a>Parametreler  
 `locid`  
 İsteğe bağlı. Yerelleştirme bilgilerini işlev veya yöntem tanımlayıcısı. Tanımlayıcıdır ya da bir üye kimliği veya karşılık gelen `name` öznitelik değeri bir ileti paketteki OpenAjax meta verileri tarafından tanımlanır. Belirtilen biçim tanımlayıcı türü bağımlı [ \<loc >](../ide/loc-javascript.md) öğesi.  
  
 `description`  
 İsteğe bağlı. İşlev veya yöntem açıklaması.  
  
## <a name="remarks"></a>Açıklamalar  
 İçeren İşlevler, ek açıklama eklemek için kullanılan öğelerin [ \<Özet >](../ide/summary-javascript.md), [ \<param >](../ide/param-javascript.md), ve [ \<döndürür >](../ide/returns-javascript.md), işlev gövdesi herhangi bir deyim önce yerleştirilmelidir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod nasıl kullanılacağını gösterir `<summary>` öğesi.  
  
```javascript  
function areaFunction(radiusParam)  
{  
    /// <summary>Determines the area of a circle when supplied a radius parameter.</summary>  
    /// <param name="radiusParam" type="Number">The radius of the circle.</param>  
    /// <returns type="Number">The area.</returns>  
    var areaVal;  
    areaVal = Math.PI * radiusParam * radiusParam;  
    return areaVal;  
}  
  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Belge Açıklamaları](../ide/xml-documentation-comments-javascript.md)
