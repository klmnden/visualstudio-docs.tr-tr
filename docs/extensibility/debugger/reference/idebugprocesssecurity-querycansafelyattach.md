---
title: IDebugProcessSecurity::QueryCanSafelyAttach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProcessSecurity::QueryCanSafelyAttach
ms.assetid: 63ec1ae8-27da-4574-aa15-1c986fe9fe58
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 891a0c200b02f8768ef68d1d87649bfd35cf59d2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60040617"
---
# <a name="idebugprocesssecurityquerycansafelyattach"></a>IDebugProcessSecurity::QueryCanSafelyAttach
Bu yöntem, kullanıcının güvenli olmayan bir işleme iliştirir önce bir uyarı görüntülenecek bağlantı noktası sağlayıcısı sağlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT QueryCanSafelyAttach();
```

```csharp
int QueryCanSafelyAttach();
```

## <a name="return-value"></a>Dönüş Değeri
 Dönüş değerleri aşağıdaki gibidir:

- `S_OK`: İşlemine iliştirme güvenlidir ve uyarı iletişim kutusu gösterilir.

- `S_FALSE`: İliştirme bir güvenlik sorunu olabilir ve bir uyarı ile bir iletişim kutusu gösterilir.

- `FAILURE`: İşlemine iliştirme başarısız.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProcessSecurity](../../../extensibility/debugger/reference/idebugprocesssecurity.md)