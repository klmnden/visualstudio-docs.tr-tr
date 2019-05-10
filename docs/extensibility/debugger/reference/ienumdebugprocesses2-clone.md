---
title: IEnumDebugProcesses2::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugProcesses2::Clone
helpviewer_keywords:
- IEnumDebugProcesses2::Clone
ms.assetid: 3d4196d3-5a80-4f76-b8b2-f72e80c8d406
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 79dcf0316905911bf60aa0f634bcd7fd245ed761
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65225811"
---
# <a name="ienumdebugprocesses2clone"></a>IEnumDebugProcesses2::Clone
Bir kopyasını ayrı bir nesne olarak geçerli bir sabit listesi döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Clone(
   IEnumDebugProcesses2** ppEnum
);
```

```csharp
int Clone(
   out IEnumDebugProcesses2 ppEnum
);
```

## <a name="parameters"></a>Parametreler
 `ppEnum`\

 [out] Bu numaralandırma ayrı bir nesne gibi bir kopyasını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Numaralandırma kopyasını bu yöntemin çağrıldığı zaman orijinal ile aynı duruma sahiptir. Ancak, kopyanın ve orijinalin durumları ayrıdır ve ayrı ayrı değiştirilebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugProcesses2](../../../extensibility/debugger/reference/ienumdebugprocesses2.md)