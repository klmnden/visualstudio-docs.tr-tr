---
title: IDebugProcessEx2::Detach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::Detach
helpviewer_keywords:
- IDebugProcessEx2::Detach method
ms.assetid: 66d54c2c-9302-47c8-9975-f30ed988ab29
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 58480e52e86fc4603648d9f534cb03e944a8dde8
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212893"
---
# <a name="idebugprocessex2detach"></a>IDebugProcessEx2::Detach
Bu yöntem, bir oturum işlemi artık hata ayıklıyor işlem bildirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Detach( 
   IDebugSession2* pSession
);
```

```csharp
int Detach(
   IDebugSession2 pSession
);
```

## <a name="parameters"></a>Parametreler
`pSession`\
[in] Bu işlemden ayırmak için oturum benzersiz olarak tanımlayan bir değer.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Arabirim geçirilen `pSession` oturum hata ayıklama Yöneticisi, başlangıçta benzersiz olarak tanımlayan bir değer yalnızca bir tanımlama bilgisi değerlendirilmesi için bu işleme bağlı; sağlanan arabirim yöntemleri hiçbiri işlevsel değildir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)