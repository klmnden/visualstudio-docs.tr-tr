---
title: IEnumDebugObjects | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugObjects
helpviewer_keywords:
- IEnumDebugObjects interface
ms.assetid: 0950364c-6c8a-4b6c-ba37-c6aa359fa72c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8a0de2742b5fee3215d1fddbe7912943effe639d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680977"
---
# <a name="ienumdebugobjects"></a>IEnumDebugObjects
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirimi uygulayan nesnelerin bir koleksiyonunu temsil eder [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugObjects : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendirici uygulayan nesne kümeleri sağlamak için bu arabirimi uygulayan [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) arabirimi. Bu varlığı nedeniyle standart bir COM numaralandırma olmadığını unutmayın [GetCount](../../../extensibility/debugger/reference/ienumdebugobjects-getcount.md) yöntemi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
- [GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md) bu arabirimi döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Bu arabirim, aşağıdaki yöntemleri uygular.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugobjects-next.md)|Sonraki alır [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesnelerden sabit listesi.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugobjects-skip.md)|Belirtilen bir girdi sayısı atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugobjects-reset.md)|Numaralandırma ilk girişe sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugobjects-clone.md)|Geçerli sabit bir kopyasını alır.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugobjects-getcount.md)|Sabit listesi içerisindeki giriş sayısını alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, dizi bir nesne üzerinden numaralandırmak bir hata ayıklama altyapısı sağlar.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md)