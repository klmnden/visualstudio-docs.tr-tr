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
ms.openlocfilehash: 7ef0ce265bc63ce9a00fd748c50a338d52294557
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211695"
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