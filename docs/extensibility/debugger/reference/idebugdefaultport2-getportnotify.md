---
title: IDebugDefaultPort2::GetPortNotify | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDefaultPort2::GetPortNotify
helpviewer_keywords:
- IDebugDefaultPort2::GetPortNotify
ms.assetid: 3ae715ee-9886-4694-a52b-59bb3b27467a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fd85f76ab0c882656ca79fe02296f30bdb83f523
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351771"
---
# <a name="idebugdefaultport2getportnotify"></a>IDebugDefaultPort2::GetPortNotify
Bu yöntem alır bir [IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md) Bu bağlantı noktası için arabirim.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetPortNotify(
   IDebugPortNotify2** ppPortNotify
);
```

```csharp
int GetPortNotify(
   out IDebugPortNotify2 ppPortNotify
);
```

## <a name="parameters"></a>Parametreler
`ppPortNotify`\
[out] Bir [IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md) nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Normalde, `QueryInterface` yöntemi, uygulama nesnesi üzerinde çağrıldığında [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimi almak için bir [IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md) arabirimi. Ancak, istendiği arayüz farklı bir nesne üzerinde uygulanmadı koşullar vardır. Bu yöntem bu koşullarda gizler ve döndürür `IDebugPortNotify2` en uygun nesnesinden arabirimi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)
- [IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md)