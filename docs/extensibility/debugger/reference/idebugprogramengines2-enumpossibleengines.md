---
title: IDebugProgramEngines2::EnumPossibleEngines | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramEngines2::EnumPossibleEngines
helpviewer_keywords:
- IDebugProgramEngines2::EnumPossibleEngines
ms.assetid: 993d70a4-f6a5-4e47-a603-0b162b9fde00
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: d226650592881e9e7f87a5fbf5c700dfd7d817cb
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211141"
---
# <a name="idebugprogramengines2enumpossibleengines"></a>IDebugProgramEngines2::EnumPossibleEngines
Bu programda hata ayıklamak tüm olası hata ayıklama altyapısı (DE) GUID'lerini döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumPossibleEngines( 
   DWORD  celtBuffer,
   GUID*  rgguidEngines,
   DWORD* pceltEngines
);
```

```csharp
int EnumPossibleEngines( 
   uint      celtBuffer,
   GUID[]    rgguidEngines,
   ref DWORD pceltEngines
);
```

## <a name="parameters"></a>Parametreler
`celtBuffer`\
[in] Döndürülecek DE GUID'leri sayısı. Bu ayrıca en büyük boyutunu belirtir `rgguidEngines` dizisi.

`rgguidEngines`\
[out içinde] Doldurulacak DE GUID'leri dizisi.

`pceltEngines`\
[out] Döndürülen DE GUID'leri gerçek sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür [C++] `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` veya [C#] 0x8007007A arabelleğin yeteri kadar büyük değil ise.

## <a name="remarks"></a>Açıklamalar
 Kaç altyapıları var olduğunu belirlemek için bu yöntemi bir kez çağırın `celtBuffer` parametresi 0 olarak ayarlayın ve `rgguidEngines` parametresi null bir değere ayarlayın. Bu döndürür `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` (0x8007007A için C#) ve `pceltEngines` parametresi gerekli arabellek boyutunu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramEngines2](../../../extensibility/debugger/reference/idebugprogramengines2.md)