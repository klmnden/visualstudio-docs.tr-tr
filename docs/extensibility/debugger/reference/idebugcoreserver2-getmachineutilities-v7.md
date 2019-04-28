---
title: IDebugCoreServer2::GetMachineUtilities_V7 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
helpviewer_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
ms.assetid: 64c1f08f-853b-4498-9810-29791581ef2f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2929ed704d8b9642d30b9a7951a707db0635b319
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63414048"
---
# <a name="idebugcoreserver2getmachineutilitiesv7"></a>IDebugCoreServer2::GetMachineUtilities_V7
Bu yöntem, bir sunucu için makine yardımcı programları alır.

> [!NOTE]
> Bu yöntem artık kullanılmıyor: kullanmayın ([!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] her zaman döndürür `E_NOTIMPL` bu yöntemi çağrılırsa). Bu, geçmiş nedenlerle korunur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetMachineUtilities_V7(
   IDebugMDMUtil2_V7** ppUtil
);
```

```csharp
int GetMachineUtilities_V7(
   out IDebugMDMUtil2_V7 ppUtil
);
```

#### <a name="parameters"></a>Parametreler
 `ppUtil`

 [out] Döndürür bir `IDebugMDMUtil2_V7` makine yardımcı programları bilgilerini temsil eden arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Her zaman döndürür `E_NOTIMPL`, belirten yöntem uygulanmadı.

## <a name="remarks"></a>Açıklamalar
 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] her zaman döndürür `E_NOTIMPL` varsa, bu yöntem çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)