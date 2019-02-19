---
title: IDebugCodeContext3::GetModule | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugCodeContext3::GetModule
ms.assetid: 8e4317b8-8255-486c-a896-a68ed94f8aa1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3f79403bfd1dfe89868b3a8e3a901e2fc370609d
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56412792"
---
# <a name="idebugcodecontext3getmodule"></a>IDebugCodeContext3::GetModule
Hata ayıklama modülü arabirimine bir başvuru alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetModule(
    IDebugModule2 **ppModule
);
```

```csharp
public int GetModule(
    out IDebugModule2 ppModule
);
```

#### <a name="parameters"></a>Parametreler
`ppModule`  
[out] Başvuru için hata ayıklama modül arabirimi.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugCodeContext** gösteren nesne [IDebugBeforeSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugbeforesymbolsearchevent2.md) arabirimi.

```cpp
HRESULT CDebugCodeContext::GetModule(IDebugModule2** ppModule)
{
    HRESULT hr = S_OK;
    CComPtr<CModule> pModule;

    IfFalseGo( ppModule, E_INVALIDARG );
    *ppModule = NULL;

    IfFailGo( this->GetModule(&pModule) );
    IfFailGo( pModule->QueryInterface(IID_IDebugModule2, (void**) ppModule) );

Error:

    return hr;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugCodeContext3](../../../extensibility/debugger/reference/idebugcodecontext3.md)
