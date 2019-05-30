---
title: IDebugCoreServer3::CreateInstanceInServer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer3::CreateInstanceInServer
helpviewer_keywords:
- IDebugCoreServer3::CreateInstanceInServer
ms.assetid: 76f36bae-f6ab-413c-a8a9-8808bfeba05b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7e74ea66f5b8ecd04acfbc2617f91bcaf0f7ecbd
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332406"
---
# <a name="idebugcoreserver3createinstanceinserver"></a>IDebugCoreServer3::CreateInstanceInServer
Sunucuda bir hata ayıklama altyapısı örneğini oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateInstanceInServer(
   LPCWSTR  szDll,
   WORD     wLangId,
   REFCLSID clsidObject,
   REFIID   riid,
   void**   ppvObject
);
```

```csharp
int CreateInstanceInServer(
   string     szDll,
   ushort     wLangID,
   ref Guid   clsidObject,
   ref Guid   riid,
   out IntPtr ppvObject
);
```

## <a name="parameters"></a>Parametreler
`szDll`\
[in] Belirtilen CLSID uygulayan dll yolu `clsidObject` parametresi. Bu ise `NULL`, ardından COM's `CoCreateInstance` işlevi çağrılır.

`wLangId`\
[in] Yerel hata ayıklama altyapısı. Bu 0 olabilir [SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md) yöntemi çağırılmalıdır.

`clsidObject`\
[in] Oluşturmak için CLSID hata ayıklama altyapısı.

`riid`\
[in] Sınıf nesneyi almak için belirli arabirimi arabirim kimliği.

`ppvObject`\
[out] `IUnknown` arabiriminden oluşturulan nesne. Cast veya istenen arabirim için bu nesnesi hazırlanamadı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)
- [SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md)