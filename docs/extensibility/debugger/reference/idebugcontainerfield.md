---
title: IDebugContainerField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugContainerField
helpviewer_keywords:
- IDebugContainerField interface
ms.assetid: a8bbe061-c382-4fe9-a193-3f7d12216041
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d633b7e42f8c7f64a818539694837b954ea31e72
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332510"
---
# <a name="idebugcontainerfield"></a>IDebugContainerField
Bu arabirim, simge veya diğer semboller veya türler için bir kapsayıcı türü temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugContainerField : IDebugField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi. Bu ayrıca kapsayıcı temsil eden tüm arabirimler için temel sınıf arabirimidir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Birçok yöntemlerde pek çok arabirimi bu arabirim döndürür. Bu, tüm kapsayıcılar için bir temel sınıfı olduğu için daha özel arabirimleri elde edilen bu arabirimden kullanarak [QueryInterface](/cpp/atl/queryinterface). Bu tür arabirimleri dahil [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md), [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md), [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md), ve [IDebugPropertyField](../../../extensibility/debugger/reference/idebugpropertyfield.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumFields](../../../extensibility/debugger/reference/idebugcontainerfield-enumfields.md)|Kapsayıcının alanlar için bir numaralandırıcı oluşturur.|

## <a name="remarks"></a>Açıklamalar
 Diziler (kapsayıcılar değişkenleri için), sınıflar (kapsayıcılar yöntemler ve değişkenler için) ve yöntemler (parametreler ve yerel değişkenler için kapsayıcılar) kapsayıcıları için tüm örnekleridir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)