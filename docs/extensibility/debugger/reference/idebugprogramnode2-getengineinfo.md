---
title: IDebugProgramNode2::GetEngineInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramNode2::GetEngineInfo
helpviewer_keywords:
- IDebugProgramNode2::GetEngineInfo
ms.assetid: 664e7fe5-9100-4b7d-9dc5-e5a4dd0d0451
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: c31d3a858af2886a27a51e22e131cb89b2234d6e
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65459077"
---
# <a name="idebugprogramnode2getengineinfo"></a>IDebugProgramNode2::GetEngineInfo
Ad ve tanımlayıcı bir programı çalıştırma hata ayıklama altyapısı (DE) alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetEngineInfo ( 
   BSTR* pbstrEngine,
   GUID* pguidEngine
);
```

```csharp
int GetEngineInfo(
   out string pbstrEngine,
   out Guid pguidEngine
);
```

## <a name="parameters"></a>Parametreler
 `pbstrEngine`\

 [out] Programın çalıştırılması DE adını döndürür (C++-belirli: Bu çağrı altyapısı adını ilgilenen değil gösteren null bir işaretçi olabilir).

 `pguidEngine`\

 [out] Programın çalıştırılması DE genel benzersiz tanımlayıcısını döndürür (C++-belirli: Bu çağırana ilişkin GUID'i altyapısının ilgilenen değil gösteren null bir işaretçi olabilir).

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)