---
title: Model öğelerine başvuru dizelerini iliştirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
helpviewer_keywords:
- UML - extending, reference strings
ms.assetid: 15dbed99-efce-42fe-a768-714a5804e7d1
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bd5a1ae4abc2e0b5c508b7b77160bbf8da3bb45e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68203219"
---
# <a name="attach-reference-strings-to-uml-model-elements"></a>Model öğelerine başvuru dizeleri ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Model öğelerine rastgele dize eklemek için kod yazabilirsiniz. Bir dize, örneğin, bir URI, bir hesaplama veya başka bir modelinde bir öğedeki ModelBus başvurusu önbelleğe alınan sonucu olabilir. Her bir dizenin IReference nesnesi içinde yer alır. Herhangi bir sayıda IReference nesneleri her model öğesine bağlı olmalıdır.  
  
 Her IReference nesne bir adı vardır. Bu ad, başvuru değeri nasıl yorumlanması gerektiğini belirtmek için kullanabilirsiniz. Örneğin, adı "URI" değeri olarak bir URI yorumlanması gerektiğini belirtmek için ayarlayabilirsiniz. Modelleme Araçları tarafından kullanılan bazı önceden tanımlı başvuru adı değerleri vardır.  
  
## <a name="attaching-a-reference-to-an-ielement"></a>Bir IElement başvuru ekleme  
 Aşağıdaki yöntemleri kullanmak için bir başvuru eklemeniz gerekir:  
  
 Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll  
  
 Kodunuzda bu yönergesi eklemeniz gerekir:  
  
 `using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml;`  
  
|Yöntem çağrısı|Açıklama|  
|-----------------|-----------------|  
|`element.AddReference (nameString, valueString, duplicatesAllowed)`|Oluşturur bir `IReference` verilen ad ve değer dizeleri ve bağlantı `element`. Döndürür `IReference`.<br /><br /> Bir özel durum oluşturur `duplicatesAllowed` false olduğundan ve zaten var. bir `IReference` bağlı aynı ada sahip `element`.|  
|`element.GetReferences(name)`|Tüm döndürür `IReference` bağlı nesneler `element` olan belirli `name`.|  
|`element.DeleteAllReferences(name)`|Tüm siler `IReference` nesneleri belirtilen ada sahip bir öğeye bağlı.|  
|`reference.Delete()`|Bu siler `IReference`.|  
|`ReferenceConstants.WorkItem`|Ad çalışma öğesi başvuruları için kullanılan değer.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bir iş öğesi bağlantı işleyicisini tanımlama](../modeling/define-a-work-item-link-handler.md)   
 [Modelleme Uzantısı Tanımlama ve yükleme](../modeling/define-and-install-a-modeling-extension.md)   
 [UML API ile programlama](../modeling/programming-with-the-uml-api.md)
