---
title: IDebugPortPicker::SetSite | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugPortPicker::SetSite
ms.assetid: 7319e187-adfe-4b3f-aec9-521356fb5a8a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: d44c0ad0cef8777623f3393172e372ea4c33782a
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66204506"
---
# <a name="idebugportpickersetsite"></a>IDebugPortPicker::SetSite
Hizmet sağlayıcısı ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetSite(
   IServiceProvider * pSP
);
```

```csharp
public int SetSite(
   IServiceProvider pSP
);
```

## <a name="parameters"></a>Parametreler
`pSP`\
[in] Hizmet sağlayıcısının arabirimi başvuru.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Diğer yöntemleri çağrılmadan önce bu yöntem çağrılır.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)