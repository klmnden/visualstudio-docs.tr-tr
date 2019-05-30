---
title: IDebugEngine2::SetException | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::SetException
helpviewer_keywords:
- IDebugEngine2::SetException
ms.assetid: e6f5ec48-09e8-4b9b-9dc9-55f8d883f1b7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 2234c0c0b571e763d3b143b5606fe61c43f25cde
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352540"
---
# <a name="idebugengine2setexception"></a>IDebugEngine2::SetException
Hata ayıklama altyapısı (DE) verilen bir özel durumun nasıl işleyeceğini belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetException( 
   EXCEPTION_INFO* pException
);
```

```csharp
int SetException( 
   EXCEPTION_INFO[] pException
);
```

## <a name="parameters"></a>Parametreler
`pException`\
[in] Bir [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md) özel durum ve hata ayıklamak nasıl açıklayan yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir DE belirtildiği bir ilk fırsat özel duruma oluşturma programı durdurun, fırsat, ikinci ya da hiç.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
- [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)