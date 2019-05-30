---
title: IDebugAlias2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugAlias2 interface
ms.assetid: 5252dcbb-8bfe-4d8a-a8e5-b022b194df19
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: abd220cd8c67318981fda79d3be8a0014ab61de1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321721"
---
# <a name="idebugalias2"></a>IDebugAlias2
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bir değişken için sayısal bir diğer adı temsil eder ve bir ifade değerlendiricisi uygulama etki alanı diğer adı için elde edilir (EE) sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugAlias2 : IDebugAlias
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim yönetilen hata ayıklama altyapısı (DE) tarafından uygulanır.

## <a name="methods"></a>Yöntemler
 Yöntemlere ek olarak [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md) arabirimi bu arabirim, aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetAppDomainId](../../../extensibility/debugger/reference/idebugalias2-getappdomainid.md)|Uygulama etki alanı için tanımlayıcıyı alır.|

## <a name="remarks"></a>Açıklamalar
 Bir diğer ad, sonrasında # karakteri, örneğin, 1001 # dize biçiminde bir ondalık sayıdır.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll