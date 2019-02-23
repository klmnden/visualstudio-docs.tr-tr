---
title: IDebugCustomAttributeQuery | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugCustomAttributeQuery interface
ms.assetid: b804b619-70eb-4c38-80d9-c8b32b65ed3e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ea9c37dbb889a622d0b428d53144c27d0c04aef9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706463"
---
# <a name="idebugcustomattributequery"></a>IDebugCustomAttributeQuery
Bir sorgu için bir yöntem veya türü özel öznitelikleri temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugCustomAttributeQuery : IUnknown
```

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetCustomAttributeByName](../../../extensibility/debugger/reference/idebugcustomattributequery-getcustomattributebyname.md)|Özel bir öznitelik adı verilen alır.|
|[IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery-iscustomattributedefined.md)|Belirler belirtilen özel özniteliğin tanımlandığından.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll