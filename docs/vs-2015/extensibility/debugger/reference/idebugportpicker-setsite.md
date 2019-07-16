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
ms.openlocfilehash: 6cd0b91491be365a4686265bd698717219df0afb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68188402"
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

#### <a name="parameters"></a>Parametreler
 `pSP`

 [in] Hizmet sağlayıcısının arabirimi başvuru.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Diğer yöntemleri çağrılmadan önce bu yöntem çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)