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
ms.openlocfilehash: 9dc3185b644a1045428ead9f2c9851916df3249c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62917038"
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

#### <a name="parameters"></a>Parametreler
 `celtBuffer`

 [in] Döndürülecek DE GUID'leri sayısı. Bu ayrıca en büyük boyutunu belirtir `rgguidEngines` dizisi.

 `rgguidEngines`

 [out içinde] Doldurulacak DE GUID'leri dizisi.

 `pceltEngines`

 [out] Döndürülen DE GUID'leri gerçek sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür [C++] `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` veya [C#] 0x8007007A arabelleğin yeteri kadar büyük değil ise.

## <a name="remarks"></a>Açıklamalar
 Kaç altyapıları var olduğunu belirlemek için bu yöntemi bir kez çağırın `celtBuffer` parametresi 0 olarak ayarlayın ve `rgguidEngines` parametresi null bir değere ayarlayın. Bu döndürür `HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)` (0x8007007A için C#) ve `pceltEngines` parametresi gerekli arabellek boyutunu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgramEngines2](../../../extensibility/debugger/reference/idebugprogramengines2.md)