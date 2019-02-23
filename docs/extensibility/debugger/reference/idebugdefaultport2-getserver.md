---
title: IDebugDefaultPort2::GetServer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDefaultPort2::GetServer
helpviewer_keywords:
- IDebugDefaultPort2::GetServer
ms.assetid: cacb4b74-0f39-471c-af38-54b73f5b2868
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2cbfc81495c1f2319117a236246f1e7c47f3e582
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678652"
---
# <a name="idebugdefaultport2getserver"></a>IDebugDefaultPort2::GetServer
Bu yöntem, bu bağlantı noktası sunucusuna bir arabirim alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetServer(
   IDebugCoreServer3** ppServer
);
```

```csharp
int GetServer(
   out IDebugCoreServer3 ppServer
);
```

#### <a name="parameters"></a>Parametreler
 `ppServer`

 [out] Döndürür bir nesneyi uygulama [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) arabirimi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) Visual Studio tarafından uygulanır ve bağlantı noktası üzerinde bulunduğu sunucu temsil eder.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)