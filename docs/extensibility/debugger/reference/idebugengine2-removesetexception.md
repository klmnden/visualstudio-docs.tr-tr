---
title: IDebugEngine2::RemoveSetException | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::RemoveSetException
helpviewer_keywords:
- IDebugEngine2::RemoveSetException
ms.assetid: bdd25097-0e9d-4218-b417-0497ea48d2e8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 52d2d628f9fcbc2279096a12117951f4c02f8bf4
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66207576"
---
# <a name="idebugengine2removesetexception"></a>IDebugEngine2::RemoveSetException
Belirtilen özel durum artık hata ayıklama altyapısı tarafından işlenecek şekilde kaldırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT RemoveSetException( 
   EXCEPTION_INFO* pException
);
```

```csharp
int RemoveSetException( 
   EXCEPTION_INFO[] pException
);
```

## <a name="parameters"></a>Parametreler
`pException`\
[in] Bir [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md) kaldırılacak özel durumu açıklayan yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kaldırılmakta olan özel durum daha önce daha önceki bir çağrı tarafından ayarlanmış olması gerekir [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md) yöntemi.

 Tüm küme özel durumları tek seferde kaldırmak için çağrı [RemoveAllSetExceptions](../../../extensibility/debugger/reference/idebugengine2-removeallsetexceptions.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
- [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)