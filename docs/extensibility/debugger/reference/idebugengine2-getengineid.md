---
title: IDebugEngine2::GetEngineID | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngine2::GetEngineID
helpviewer_keywords:
- IDebugEngine2::GetEngineID
ms.assetid: 0d5674c8-a9b9-4b72-8211-d2d68695775a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 09863abc81d3f4f1a5e4e541c9e0019d30156b67
ms.sourcegitcommit: 845442e2b515c3ca1e4e47b46cc1cef4df4f08d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56449639"
---
# <a name="idebugengine2getengineid"></a>IDebugEngine2::GetEngineID
Hata ayıklama altyapısı (DE) GUID alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetEngineID(
    GUID* pguidEngine
);
```

```csharp
int GetEngineID(
    out Guid pguidEngine
);
```

#### <a name="parameters"></a>Parametreler
`pguidEngine`  
[out] DE GUİD'sini döndürür.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Tipik GUID'leri bazı örnekleri şunlardır `guidScriptEng`, `guidNativeEng`, veya `guidSQLEng`. Yeni hata ayıklama altyapıları kendi kimlik GUİD'i oluşturacaksınız.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CEngine` uygulayan nesne [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) arabirimi.

```cpp
HRESULT CEngine::GetEngineId(GUID *pguidEngine) {
    if (pguidEngine) {
        // Set pguidEngine to guidBatEng, as defined in the Batdbg.idl file.
        // Other languages would require their own guidDifferentEngine to be
        //defined in the Batdbg.idl file.
        *pguidEngine = guidBatEng;
        return NOERROR; // This is typically S_OK.
    } else {
        return E_INVALIDARG;
    }
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
