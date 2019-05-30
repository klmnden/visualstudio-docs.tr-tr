---
title: IDebugBinder3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder3
helpviewer_keywords:
- IDebugBinder3 interface
ms.assetid: 92353a74-dc74-4f93-8762-61d6b220478c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 97e3165be9d478d08f4de7eb623de5b93fd3433a
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66330861"
---
# <a name="idebugbinder3"></a>IDebugBinder3
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim, türleri, diğer adlar ve özel Görselleştirici hizmetlere erişim sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugBinder3 : IDebugBinder
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı, diğer adlar, özel Görselleştirici Hizmetleri ve nesne türü bilgilerini erişimi desteklemek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) arabirimini kullanarak bu arabirimi edinir [QueryInterface](/cpp/atl/queryinterface).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Tarafından sağlanan yöntemleri yanı sıra [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) aşağıdaki arabirimi bu arabirim uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetMemoryObject](../../../extensibility/debugger/reference/idebugbinder3-getmemoryobject.md)|Bu nesne, bağlı olduğu bellek temsil eden bir bellek nesnesi alır.|
|[GetExceptionObjectAndType](../../../extensibility/debugger/reference/idebugbinder3-getexceptionobjectandtype.md)|(Varsa) Bu nesneyle ilişkili özel durumu alır,|
|[FindAlias](../../../extensibility/debugger/reference/idebugbinder3-findalias.md)|Adı verilen bir diğer ad alır,|
|[GetAllAliases](../../../extensibility/debugger/reference/idebugbinder3-getallaliases.md)|Bu nesne için tüm diğer adlarını alır,|
|[GetTypeArgumentCount](../../../extensibility/debugger/reference/idebugbinder3-gettypeargumentcount.md)|Bu nesneyle ilişkili bağımsız değişken türleri sayısını alır,|
|[GetTypeArguments](../../../extensibility/debugger/reference/idebugbinder3-gettypearguments.md)|Bu nesneyle ilişkili bağımsız değişken türlerinin bir listesini alır,|
|[GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md)|Görselleştirici hizmeti için bir arabirim alır,|
|[GetMemoryContext64](../../../extensibility/debugger/reference/idebugbinder3-getmemorycontext64.md)|Bir nesnenin konumu veya 64-bit bellek adresi bellek bağlamına dönüştürür.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)