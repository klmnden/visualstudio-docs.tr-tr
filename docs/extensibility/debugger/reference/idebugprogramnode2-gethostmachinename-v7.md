---
title: IDebugProgramNode2::GetHostMachineName_V7 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramNode2::GetHostMachineName
helpviewer_keywords:
- IDebugProgramNode2::GetHostMachineName_V7
- IDebugProgramNode2::GetHostMachineNameIDebugProgramNode2::GetHostMachineName
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4518ab3e4a4ee978c296815a81d8fbffb3e20db7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53966658"
---
# <a name="idebugprogramnode2gethostmachinenamev7"></a>IDebugProgramNode2::GetHostMachineName_V7

> [!Note]
> KULLANIM DIŞI. KULLANMAYIN.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetHostMachineName_V7 (
   BSTR* pbstrHostMachineName
);
```

```csharp
int GetHostMachineName_V7 (
   out string pbstrHostMachineName
);
```

#### <a name="parameters"></a>Parametreler

`pbstrHostMachineName`  
[out] Programın çalıştığı bilgisayarın adını döndürür.

## <a name="return-value"></a>Dönüş Değeri

Bir uygulama her zaman döndürmelidir `E_NOTIMPL`.

## <a name="remarks"></a>Açıklamalar

> [!WARNING]
> Visual Studio 2005 ' ten itibaren bu yöntem artık kullanılmamaktadır ve her zaman döndürmelidir `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca Bkz.

[IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)