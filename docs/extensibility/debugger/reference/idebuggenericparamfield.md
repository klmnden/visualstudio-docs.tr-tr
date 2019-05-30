---
title: IDebugGenericParamField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugGenericParamField interface
ms.assetid: ba24f499-5ba7-4c67-83e6-923229b52327
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: db5f82944063abc3274840e820104a7737944047
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66349208"
---
# <a name="idebuggenericparamfield"></a>IDebugGenericParamField
Yönetilen kod genel bir tür için bir parametreyi temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugGenericParamField : IDebugField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Genel türler için destek kullanılır.

## <a name="methods"></a>Yöntemler
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[ConstraintCount](../../../extensibility/debugger/reference/idebuggenericparamfield-constraintcount.md)|Bu genel parametre ile ilişkili olan kısıtlamaları sayısını döndürür.|
|[GetConstraints](../../../extensibility/debugger/reference/idebuggenericparamfield-getconstraints.md)|Bu genel parametre ile ilişkili olan kısıtlamaları alır.|
|[GetFlags](../../../extensibility/debugger/reference/idebuggenericparamfield-getflags.md)|Bu genel parametresi için bayrakları alır.|
|[GetIndex](../../../extensibility/debugger/reference/idebuggenericparamfield-getindex.md)|Bu genel parametre dizinini alır.|
|[GetNameOfFormalParam](../../../extensibility/debugger/reference/idebuggenericparamfield-getnameofformalparam.md)|Bu genel parametre adını alır.|
|[GetOwner](../../../extensibility/debugger/reference/idebuggenericparamfield-getowner.md)|Bu genel parametre türü veya yönteminde sahibi alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll