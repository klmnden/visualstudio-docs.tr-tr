---
title: GetVstoSolutionMetadata işlevi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d7714e78e897e6c8b391a6c30e9a548671ce80c4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62796047"
---
# <a name="getvstosolutionmetadata-function"></a>GetVstoSolutionMetadata işlevi
  Bu API Office altyapısını destekler ve doğrudan kodunuzdan kullanılmaya yönelik değildir.

## <a name="syntax"></a>Sözdizimi

```csharp
HRESULT WINAPI GetVstoSolutionMetadata(
    LPCWSTR lpwszSolutionMetadataKey,
    ISolutionMetadata** ppSolutionInfo
);
```

### <a name="parameters"></a>Parametreler

|Parametre|Açıklama|
|---------------|-----------------|
|*lpwszSolutionMetadataKey*|Kullanmayın.|
|*ppSolutionInfo*|Kullanmayın.|

## <a name="return-value"></a>Dönüş değeri
 İşlev başarılı olursa, döndürür **S_OK**. İşlev başarısız olursa hata kodu döndürür.
