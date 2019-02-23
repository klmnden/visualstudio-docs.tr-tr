---
title: IDebugEngine2::DestroyProgram | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::DestroyProgram
helpviewer_keywords:
- IDebugEngine2::DestroyProgram
ms.assetid: 0c9e2698-c70f-4770-a7bb-39650e9c3a1f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f626005621604d367f5878e36899aa2ff46114ee
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678455"
---
# <a name="idebugengine2destroyprogram"></a>IDebugEngine2::DestroyProgram
Belirtilen program beklenmedik şekilde sona erdi ve DE program için tüm başvuruları temizlemek bir hata ayıklama altyapısı (DE) bildirir ve olay gönderme bir program yok.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT DestroyProgram( 
   IDebugProgram2* pProgram
);
```

```cpp
int DestroyProgram( 
   IDebugProgram2 pProgram
);
```

#### <a name="parameters"></a>Parametreler
 `pProgram`

 [in] Bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) beklenmedik şekilde sonlandırıldı program temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntemi çağrıldıktan sonra DE sonradan gönderir bir [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) olay oturumu hata ayıklama Yöneticisi (SDM) geri dönün.

 Bu yöntem uygulanmadı (döndürür `E_NOTIMPL`) DE aynı işlemde hata ayıklanan programa olarak çalışıyorsa. Bu yöntem, yalnızca DE aynı işlemde SDM olarak çalışıyorsa uygulanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
- [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)