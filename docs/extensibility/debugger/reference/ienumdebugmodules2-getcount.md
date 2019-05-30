---
title: IEnumDebugModules2::GetCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugModules2::GetCount
helpviewer_keywords:
- IEnumDebugModules2::GetCount
ms.assetid: f4def3d2-7cc9-4cd2-9649-3b7e00a76220
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b46198507eac96144583d86fcde1f1a1718fe15b
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350253"
---
# <a name="ienumdebugmodules2getcount"></a>IEnumDebugModules2::GetCount
Numaralandırmada öğelerin sayısını döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCount(
   ULONG* pcelt
);
```

```csharp
int GetCount(
   out uint pcelt
);
```

## <a name="parameters"></a>Parametreler
`pcelt`\
[out] Numaralandırmada öğelerin sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem yalnızca belirten geleneksel COM numaralandırma arabiriminin bir parçası değil `Next`, `Clone`, `Skip`, ve `Reset` yöntemleri uygulanması gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)