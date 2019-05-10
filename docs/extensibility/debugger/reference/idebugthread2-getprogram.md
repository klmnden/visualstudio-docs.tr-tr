---
title: IDebugThread2::GetProgram | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetProgram
helpviewer_keywords:
- IDebugThread2::GetProgram
ms.assetid: 8c9c5ea1-2031-472e-bc8f-30e22e754566
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 44f673690341c6a20b250f401265fe2db9fd5727
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65224102"
---
# <a name="idebugthread2getprogram"></a>IDebugThread2::GetProgram
Bir iş parçacığı çalıştığı program alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetProgram ( 
   IDebugProgram2** ppProgram
);
```

```csharp
int GetProgram ( 
   out IDebugProgram2 ppProgram
);
```

## <a name="parameters"></a>Parametreler
 `ppProgram`\

 [out] Döndürür bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) bu iş parçacığı çalışıyor program temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)