---
title: IDebugProcess3::DisableENC | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess3::DisableENC
helpviewer_keywords:
- IDebugProcess3::DisableENC
ms.assetid: cffdbdac-4d76-4aeb-aa55-5d0410db99f1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 39b7456d9a045331c53f8465cc7387823c734104
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688933"
---
# <a name="idebugprocess3disableenc"></a>IDebugProcess3::DisableENC
Bu yöntemi açıkça devre dışı düzenleyin ve bu işlemi devam (ve tüm programlar içerir). Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT DisableENC(
   EncUnavailableReason reason
);
```

```csharp
   EncUnavailableReason reason
);
```

#### <a name="parameters"></a>Parametreler
 `reason`

 [in] Bir değer [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md) sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

> [!NOTE]
>  Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.

## <a name="remarks"></a>Açıklamalar
 Düzenleme ve devam et için bir işlemi devre dışı bırakıldı, bu işlem yalnızca yeniden başlatarak yeniden etkinleştirilebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)
- [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md)