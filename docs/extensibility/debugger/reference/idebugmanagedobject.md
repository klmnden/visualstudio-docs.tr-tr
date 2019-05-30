---
title: IDebugManagedObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugManagedObject
helpviewer_keywords:
- IDebugManagedObject interface
ms.assetid: 3ae09d34-112c-4285-80ee-9f7f8dc414d7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6744ae98a0210a6832bce1bdb0cd68f08145f3eb
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66349409"
---
# <a name="idebugmanagedobject"></a>IDebugManagedObject
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İfade değerlendirici özellikleri veya yöntemleri değer sınıfı örneklerinde çağrılacak (EE) Bu arabirim sağlar (örneğin, `System.Decimal`) ve değerlerine çağırmadan ayarlamak için [değerlendir](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md) temel ayıklanan programa.

## <a name="syntax"></a>Sözdizimi

```
IDebugManagedObject : IDebugObject
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendiricisi, bir değişken gibi bir yönetilen kod nesnesi temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim elde etmek için çağrı [GetManagedDebugObject](../../../extensibility/debugger/reference/idebugobject-getmanageddebugobject.md) üzerinde bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) temsil eden bir değer sınıfının örneği.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md), `IDebugManagedObject` arabirimi aşağıdaki yöntemleri sunar.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject-getmanagedobject.md)|Hangi tüm uygun yönetilen koddan arabirimi alınabilir ve yönetilen kod nesnesini temsil eden bir arabirim döndürür.|
|[SetFromManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject-setfrommanagedobject.md)|Bu nesne değeri belirtilen yönetilen kod nesnesi olarak ayarlar.|

## <a name="remarks"></a>Açıklamalar
 İfade değerlendiricisi, ayrıştırma ağacı içinde yönetilen kod nesne depolamak için bu arabirimi kullanır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [Evaluate](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md)