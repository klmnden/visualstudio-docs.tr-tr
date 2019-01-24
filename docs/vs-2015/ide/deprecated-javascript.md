---
title: '&lt;kullanım dışı&gt; (JavaScript) | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: cf33d371-59da-4310-95ee-d7524fd9d58c
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b93a2b4dcc541f32c16766da0dd9dd19a4fdfe0d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54759762"
---
# <a name="ltdeprecatedgt-javascript"></a>&lt;kullanım dışı&gt; (JavaScript)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir kullanım dışı işlev veya metot belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
<deprecated  
    type="deprecate|remove"  
    locid="descriptionID">description  
</deprecated>  
```  
  
#### <a name="parameters"></a>Parametreler  
 `type`  
 İsteğe bağlı. İşlev veya yöntem gelecekteki bir sürümde olup olmadığını kaldırılacak veya olup işlev veya yöntem zaten kaldırıldı ve kullanımını hataya neden belirtir. Kümesine `deprecate` işlev veya yöntem gelecekteki bir sürümde kaldırılacak belirtmek için. Kümesine `remove` işlev veya yöntem zaten kaldırıldığını belirtmek için.  
  
 `locid`  
 İsteğe bağlı. Yerelleştirme bilgilerini işlev veya yöntem tanımlayıcısı. Tanımlayıcıdır ya da bir üye kimliği veya karşılık gelen `name` öznitelik değeri bir ileti paketteki OpenAjax meta verileri tarafından tanımlanır. Belirtilen biçim tanımlayıcı türü bağımlı [ \<loc >](../ide/loc-javascript.md) öğesi.  
  
 `description`  
 İsteğe bağlı. İşlev veya kullanım dışı yöntem açıklaması.  
  
## <a name="remarks"></a>Açıklamalar  
 İçeren İşlevler, ek açıklama eklemek için kullanılan öğelerin `<deprecated>`, işlev gövdesinin herhangi bir deyim önce yerleştirilmelidir. Bir işlev kullanım dışı olarak işaretlediğinizde, değiştirmeniz önerilir, [ \<Özet >](../ide/summary-javascript.md) öğeyle `<deprecated>` öğesi.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod nasıl kullanılacağını gösterir `<deprecated>` öğesi.  
  
```javascript  
function areaFunction(radiusParam) {  
    /// <deprecated type="deprecate" >Determines the area of a circle when supplied a radius parameter.</deprecated>  
    /// <param name="radiusParam" type="Number">The radius of the circle.</param>  
    /// <returns type="Number">The area.</returns>  
    var areaVal;  
    areaVal = Math.PI * radiusParam * radiusParam;  
    return areaVal;  
}  
  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Belge Açıklamaları](../ide/xml-documentation-comments-javascript.md)
