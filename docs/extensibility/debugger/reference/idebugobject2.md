---
title: IDebugObject2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2
helpviewer_keywords:
- IDebugObject2 interface
ms.assetid: ef640967-8adb-4793-994d-ae1736510891
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d3f027fd08c38433d5f1357e56d90df96e223854
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317259"
---
# <a name="idebugobject2"></a>IDebugObject2
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim, bir nesne hakkında ek bilgi sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugObject2 : IDebugObject
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendirici, diğer adlar ve nesne ile ilgili bilgilere erişim için destek sunmak için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) kullanarak arabirimi bu arabirim edinebilirsiniz [QueryInterface](/cpp/atl/queryinterface). Ayrıca, [GetObject](../../../extensibility/debugger/reference/idebugalias-getobject.md) bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) arabirimi `IDebugObject2` aşağıdaki arabirim uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetBackingFieldForProperty](../../../extensibility/debugger/reference/idebugobject2-getbackingfieldforproperty.md)|Alan veya değişken (varsa) alır, yedekleme bu nesne tarafından temsil edilen özelliği.|
|[GetICorDebugValue](../../../extensibility/debugger/reference/idebugobject2-geticordebugvalue.md)|Bu nesnenin değerini temsil eden yönetilen kod nesnesi alır.|
|[CreateAlias](../../../extensibility/debugger/reference/idebugobject2-createalias.md)|Bu nesne için bir benzersiz kimlik oluşturur veya mevcut bir diğer adı döndürür.|
|[GetAlias](../../../extensibility/debugger/reference/idebugobject2-getalias.md)|Bu nesneyle ilişkilendirilmiş diğer ada varsa alır.|
|[GetField](../../../extensibility/debugger/reference/idebugobject2-getfield.md)|Bu nesne türünü alır.|
|[IsUserData](../../../extensibility/debugger/reference/idebugobject2-isuserdata.md)|Bu nesne kullanıcı verilerini temsil edip etmediğini belirler.|
|[IsEncOutdated](../../../extensibility/debugger/reference/idebugobject2-isencoutdated.md)|Düzenle ve devam et durumu artık geçerli olup olmadığını belirler.<br /><br /> Özel ifade değerlendiricisi, bu yöntem uygulamaz (her zaman döndürmelidir `E_NOTIMPL`).|

## <a name="remarks"></a>Açıklamalar
 Bkz: [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) diğer adlar hakkındaki bir tartışmaya.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)
- [GetObject](../../../extensibility/debugger/reference/idebugalias-getobject.md)