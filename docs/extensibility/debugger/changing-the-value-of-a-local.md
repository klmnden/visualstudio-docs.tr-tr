---
title: Yerel bir değerinin değiştirilmesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, changing values programmatically
ms.assetid: 8407d3df-d38a-4328-82d1-98084bef43ec
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 998200420cf2ec5e0b021a415cdb9d287b1362db
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66349750"
---
# <a name="change-the-value-of-a-local"></a>Yerel bir değiştirin
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Ne zaman yeni bir değer yazıldığında değer alanına **Yereller** penceresinde, hata ayıklama paketi geçirir, dize, ifade değerlendiricisi (EE) yazılı olarak. EE basit değer veya ifade içerebilir ve ilişkili yerel sonuç değerini depolar Bu dize değerlendirir.

 Bu yerel değerini değiştirme işlemine bir genel bakış.

1. Kullanıcı yeni bir değer girdikten sonra Visual Studio çağırır [SetValueAsString](../../extensibility/debugger/reference/idebugproperty2-setvalueasstring.md) üzerinde [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) yerel ile ilişkili nesne.

2. `IDebugProperty2::SetValueAsString` Aşağıdaki görevleri gerçekleştirir:

   1. Dize değeri üretmek için değerlendirir.

   2. İlişkili bağlar [IDebugField](../../extensibility/debugger/reference/idebugfield.md) nesne elde etmek için bir [IDebugObject](../../extensibility/debugger/reference/idebugobject.md) nesne.

   3. Değer bir dizi bayt dönüştürür.

   4. Çağrıları [SetValue](../../extensibility/debugger/reference/idebugobject-setvalue.md) ayıklanan programa erişebilmesi için bu değerin bayt belleğe yerleştirmek için.

3. Visual Studio yeniler **Yereller** görüntüleme (bkz [görüntüleme Yereller](../../extensibility/debugger/displaying-locals.md) Ayrıntılar için).

   Bu yordam içinde bir değişken değerini değiştirmek için de kullanılır **Watch** bunun dışında penceresinde `IDebugProperty2` yerine kullanılan yerel değeriyle ilişkili nesne `IDebugProperty2` yerel ile ilişkili nesne kendisi.

## <a name="in-this-section"></a>Bu bölümde
 [Değer değiştirme örnek uygulaması](../../extensibility/debugger/sample-implementation-of-changing-values.md) değerlerini değiştirme işleminde size adım adım MyCEE örnek kullanır.

## <a name="see-also"></a>Ayrıca bkz.
- [Bir CLR ifade değerlendiricisi yazma](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)
- [Yerel öğeleri görüntüleme](../../extensibility/debugger/displaying-locals.md)