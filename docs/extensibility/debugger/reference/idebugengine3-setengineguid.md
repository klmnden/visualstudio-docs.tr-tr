---
title: IDebugEngine3::SetEngineGuid | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine3::SetEngineGuid
helpviewer_keywords:
- IDebugEngine3::SetEngineGuid
ms.assetid: 8bdfa05d-feb7-4d98-abac-77825a04c50f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 8881e2928ed112230ba00fafc6526962bdeb5a4e
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66207419"
---
# <a name="idebugengine3setengineguid"></a>IDebugEngine3::SetEngineGuid
Bu yöntem, hata ayıklama altyapısının (DE) ayarlar `GUID`.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetEngineGuid(
   GUID* guidEngine
);
```

```csharp
int SetEngineGuid(
   ref Guid guidEngine
);
```

## <a name="parameters"></a>Parametreler
`guidEngine`\
[in] `GUID` altyapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)