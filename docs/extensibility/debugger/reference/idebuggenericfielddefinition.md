---
title: IDebugGenericFieldDefinition | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugGenericFieldDefinition interface
ms.assetid: b5a853b7-221e-4d62-8948-07423089d75d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2887333789a9a4eae89a9f3f7538cf5b29ba02e7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351248"
---
# <a name="idebuggenericfielddefinition"></a>IDebugGenericFieldDefinition
Yönetilen kod genel bir tür için bir alan tanımını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugGenericFieldDefinition : IUnknown
```

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[ConstructInstantiation](../../../extensibility/debugger/reference/idebuggenericfielddefinition-constructinstantiation.md)|Tür bağımsız değişkenleri dizisini verilen bir alanda örneği oluşturur.|
|[GetFormalTypeParams](../../../extensibility/debugger/reference/idebuggenericfielddefinition-getformaltypeparams.md)|Parametre sayısı belirtilen tür parametreleri alır.|
|[TypeParamCount](../../../extensibility/debugger/reference/idebuggenericfielddefinition-typeparamcount.md)|Tür parametreleri genel bir alanla ilişkili sayısını alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll