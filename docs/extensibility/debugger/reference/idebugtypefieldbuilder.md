---
title: IDebugTypeFieldBuilder | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugTypeFieldBuilder interface
ms.assetid: 2dfed0be-6972-4bec-baec-f0b78df9ef97
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 456fe2656949e0cc862acdb97149b85f037beac8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56720123"
---
# <a name="idebugtypefieldbuilder"></a>IDebugTypeFieldBuilder
Türünü temsil eden bir alan oluşturma özelliği temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugTypeFieldBuilder : IUnknown
```

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, sembol Sağlayıcısı'ndan elde edilir.

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[CreatePrimitive](../../../extensibility/debugger/reference/idebugtypefieldbuilder-createprimitive.md)|Temel türünü temsil eden bir nesne oluşturur.|
|[CreatePointerToType](../../../extensibility/debugger/reference/idebugtypefieldbuilder-createpointertotype.md)|Belirtilen tür işaretçisi oluşturur.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll