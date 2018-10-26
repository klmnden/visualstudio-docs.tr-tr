---
title: Yerel bir değerinin değiştirilmesi | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, changing values programmatically
ms.assetid: 8407d3df-d38a-4328-82d1-98084bef43ec
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8f07801b22086aa9a1e96a2efc99093a84bc72e9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49843660"
---
# <a name="changing-the-value-of-a-local"></a>Yerel Bir Öğenin Değerini Değiştirme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Ne zaman yeni bir değer yazıldığında değer alanına **Yereller** penceresinde, hata ayıklama paketi geçirir, dize, ifade değerlendiricisi (EE) yazılı olarak. EE basit değer veya ifade içerebilir ve ilişkili yerel sonuç değerini depolar Bu dize değerlendirir.  
  
 Bu yerel değerini değiştirme işlemine bir genel bakış.  
  
1. Kullanıcı yeni bir değer girdikten sonra Visual Studio çağırır [SetValueAsString](../../extensibility/debugger/reference/idebugproperty2-setvalueasstring.md) üzerinde [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) yerel ile ilişkili nesne.  
  
2. `IDebugProperty2::SetValueAsString` Aşağıdaki görevleri gerçekleştirir:  
  
   1.  Dize değeri üretmek için değerlendirir.  
  
   2.  İlişkili bağlar [IDebugField](../../extensibility/debugger/reference/idebugfield.md) nesne elde etmek için bir [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) nesne.  
  
   3.  Değer bir dizi bayt dönüştürür.  
  
   4.  Çağrıları [SetValue](../../extensibility/debugger/reference/idebugobject-setvalue.md) ayıklanan programa erişebilmesi için bu değerin bayt belleğe yerleştirmek için.  
  
3. Visual Studio yeniler **Yereller** görüntüleme (bkz [görüntüleme Yereller](../../extensibility/debugger/displaying-locals.md) Ayrıntılar için).  
  
   Bu yordam içinde bir değişken değerini değiştirmek için de kullanılır **Watch** penceresi dışında `IDebugProperty2` yerine kullanılan yerel değeriyle ilişkili nesne `IDebugProperty2` yerel ile ilişkili nesne kendisi.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Örnek Değer Değiştirme Uygulaması](../../extensibility/debugger/sample-implementation-of-changing-values.md)  
 Değerleri değiştirme işleminde size adım adım MyCEE örnek kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bir CLR ifade değerlendiricisi yazma](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)   
 [Yerel Öğeleri Görüntüleme](../../extensibility/debugger/displaying-locals.md)

