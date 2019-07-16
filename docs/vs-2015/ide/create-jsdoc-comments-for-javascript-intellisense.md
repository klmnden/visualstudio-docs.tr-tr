---
title: JavaScript IntelliSense için JSDoc açıklamaları oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: a0dadc81-3755-4a47-bcee-c1010819ff2a
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f4d300651731b38b9b86421d36d9de169dc6464d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68188787"
---
# <a name="create-jsdoc-comments-for-javascript-intellisense"></a>JavaScript IntelliSense için JSDoc Açıklamaları Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio IntelliSense standart JSDoc yorumları kullanarak bir komut dosyasına eklediğiniz bilgileri görüntüler. JSDoc yorumları, İşlevler, alanları ve değişkenler gibi kod öğeleri hakkında bilgi sağlamak için kullanabilirsiniz.  

## <a name="jsdoc-comment-tags"></a>JSDoc açıklama etiketleri  
 Aşağıdaki standart JSDoc açıklama etiketleri IntelliSense tarafından kodunuz hakkında bilgileri görüntülemek için kullanılır.  

|  JSDoc etiketi   |                       Sözdizimi                        |                                                     Notlar                                                      |
|--------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| @deprecated  |              @deprecated *Açıklaması*              |                                   Bir kullanım dışı işlev veya metot belirtir.                                   |
| @description |             @description *Açıklaması*              |                              Bir işlev veya metot için açıklamayı belirtir.                               |
|    @param    | @param {*türü*} *parameterName*<em>açıklaması</em> | Bir işlev veya yöntem parametre bilgilerini belirtir.<br /><br /> TypeScript da destekler @paramTag. |
|  @property   |          @property {*türü*} *propertyName*          |   Bir alan veya bir nesne üzerinde tanımlanan üyesi için bir açıklama bilgilerini belirtir.    |
|   @returns   |                  @returns {*türü*}                  |           Dönüş değeri belirtir.<br /><br /> TypeScript için kullanmak @returnType yerine @returns.           |
|   @summary   |               @summary *Açıklaması*                |                   Bir işlev veya metot için açıklamayı belirtir (aynı @description).                   |
|    @type     |                   @type {*türü*}                    |                                Bir sabit veya değişken türünü belirtir.                                |
|   @typedef   |         @typedef {*türü*} *customTypeName*          |                                            Özel bir türünü belirtir.                                            |

### <a name="examples"></a>Örnekler  
 Aşağıdaki örnek kullanımını gösterir @description, @param, ve @return JSDoc adlı bir işlev için etiketler `getArea`.  

```javascript  
/** @description Determines the area of a circle that has the specified radius parameter.  
 * @param {number} radius The radius of the circle.  
 * @return {number}  
 */  
function getArea(radius) {  
    var areaVal;  
    areaVal = Math.PI * radius * radius;  
    return areaVal;  
}  
```  

 Bir açma parantezi için önceki örnekte, IntelliSense açıklama, parametre ve dönüş bilgi gösterilir `getArea`.  

 ![Bir işlev için IntelliSense bilgisi](../ide/media/js-intellisense-jsdoc-comments.png "JS_IntelliSense_JSDoc_Comments")  

 Aşağıdaki örnek nasıl kullanılacağını gösterir @typedef ile etiketi @property etiketi.  

```javascript  
/**  
  * @typedef {object} Weather  
  * @property {string} current The current weather.  
  */  
function getForecast(Weather) {  
}  

var w = new Weather();  
```  

 Aşağıdaki örnek kullanımını gösterir @type JSDoc etiketler. Bu örnekte gösterildiği gibi ilk yıldız çifti izleyin yıldız işareti (*) tek (\*\*) gerekli değildir.  

```javascript  
/**  
    @type {string}  
*/  
const RED = 'FF0000';  

```  

 Aşağıdaki örnek nasıl kullanılacağını gösterir @deprecated JSDoc etiketi.  

```javascript  
/**  
 * @deprecated since version 2.0  
 */  
function old() {  
}  
```
