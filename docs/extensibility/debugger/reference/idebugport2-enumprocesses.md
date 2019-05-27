---
title: IDebugPort2::EnumProcesses | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2::EnumProcesses
helpviewer_keywords:
- IDebugPort2::EnumProcesses
ms.assetid: aafb32c5-5790-4807-a448-878a80256438
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 258a31a20a53dfdf9b9573a7a8fb9f53be1fc9ac
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66209326"
---
# <a name="idebugport2enumprocesses"></a>IDebugPort2::EnumProcesses
Bir bağlantı noktası üzerinde çalışan tüm işlemlerin listesini döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumProcesses( 
   IEnumDebugProcesses2** ppEnum
);
```

```csharp
int EnumProcesses( 
   out IEnumDebugProcesses2 ppEnum
);
```

## <a name="parameters"></a>Parametreler
`ppEnum`\
[out] Döndürür bir [IEnumDebugProcesses2](../../../extensibility/debugger/reference/ienumdebugprocesses2.md) bir bağlantı noktası üzerinde çalışan tüm işlemlerin listesini içeren nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IEnumDebugProcesses2](../../../extensibility/debugger/reference/ienumdebugprocesses2.md)