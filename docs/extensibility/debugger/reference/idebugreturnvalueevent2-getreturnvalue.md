---
title: IDebugReturnValueEvent2::GetReturnValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReturnValueEvent2::GetReturnValue
helpviewer_keywords:
- IDebugReturnValueEvent2::GetReturnValue
ms.assetid: 86c50d5a-6df6-4798-818a-c587a8741f90
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: db7199a4e589d4839e2a9171350063d2bb4f9f68
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457443"
---
# <a name="idebugreturnvalueevent2getreturnvalue"></a>IDebugReturnValueEvent2::GetReturnValue
Şirket dışı veya bir işlevin üzerinden Adımlama döndürülen değer alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetReturnValue ( 
   IDebugProperty2** ppReturnValue
);
```

```csharp
int GetReturnValue ( 
   out IDebugProperty2 ppReturnValue
);
```

## <a name="parameters"></a>Parametreler
 `ppReturnValue`\

 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) alınacak değerini temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugReturnValueEvent2](../../../extensibility/debugger/reference/idebugreturnvalueevent2.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)