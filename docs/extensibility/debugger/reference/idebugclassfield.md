---
title: IDebugClassField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField
helpviewer_keywords:
- IDebugClassField interface
ms.assetid: 49358cbc-8973-4862-9dcc-79b1248e6712
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 05d01ee3867481b8ab9bb100f2623c1197492666
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329460"
---
# <a name="idebugclassfield"></a>IDebugClassField
Bu arabirim türünde bir sınıfı temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugClassField : IDebugContainerField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) arabirimi. Bu sınıf türünü temsil eden bir özelleştirmesi arabirimidir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir sayıda arabirimine sahip dahil bu arabirimi döndüren yöntemler [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md), [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md), ve [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md). Ayrıca kullanabileceğiniz [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) , arabirim [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) yöntemi bayrağı döndürür `FIELD_TYPE_CLASS`.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) ve [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) aşağıdaki arabirimleri, bu arabirimi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumBaseClasses](../../../extensibility/debugger/reference/idebugclassfield-enumbaseclasses.md)|Bu sınıfın temel sınıfları için bir numaralandırıcı oluşturur.|
|[DoesInterfaceExist](../../../extensibility/debugger/reference/idebugclassfield-doesinterfaceexist.md)|Belirli bir arabirim sınıfta tanımlı olup olmadığını belirler.|
|[EnumNestedClasses](../../../extensibility/debugger/reference/idebugclassfield-enumnestedclasses.md)|Bu sınıfın iç içe geçmiş sınıflar için bir numaralandırıcı oluşturur.|
|[GetEnclosingClass](../../../extensibility/debugger/reference/idebugclassfield-getenclosingclass.md)|Bu sınıfın kapsayan sınıf alır.|
|[EnumInterfacesImplemented](../../../extensibility/debugger/reference/idebugclassfield-enuminterfacesimplemented.md)|Bu sınıf tarafından uygulanan arabirimler için bir numaralandırıcı oluşturur.|
|[EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md)|Bu sınıfın oluşturucuları için bir numaralandırıcı oluşturur.|
|[GetDefaultIndexer](../../../extensibility/debugger/reference/idebugclassfield-getdefaultindexer.md)|Varsayılan oluşturucunun adını alır.|
|[EnumNestedEnums](../../../extensibility/debugger/reference/idebugclassfield-enumnestedenums.md)|Bu sınıfın iç içe geçmiş numaralandırıcılar için bir numaralandırıcı oluşturur.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)