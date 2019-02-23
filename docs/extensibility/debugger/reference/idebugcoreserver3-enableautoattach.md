---
title: IDebugCoreServer3::EnableAutoAttach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer3::EnableAutoAttach
helpviewer_keywords:
- IDebugCoreServer3::EnableAutoAttach
ms.assetid: 06aa633b-263b-4e08-8844-9a52d5120b94
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e6c1bf5f210d9b37b35d43a393a25b1c9df44a7e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691273"
---
# <a name="idebugcoreserver3enableautoattach"></a>IDebugCoreServer3::EnableAutoAttach
Belirtilen hata ayıklama altyapılarını otomatik iliştirme sağlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnableAutoAttach(
   GUID*     rgguidSpecificEngines,
   DWORD     celtSpecificEngines,
   LPCOLESTR pszStartPageUrl,
   BSTR*     pbstrSessionId
);
```

```csharp
int EnableAutoAttach(
   Guid[]     rgguidSpecificEngines,
   uint       celtSpecificEngines,
   string     pszStartPageUrl,
   out string pbstrSessionId
);
```

#### <a name="parameters"></a>Parametreler
 `rgguidSpecificEngines`

 [in] Her hata ayıklama altyapısı otomatik iliştirme olarak işaretlemek için GUID'lere dizisi.

 `celtSpecificEngines`

 [in] Belirtilen alt yapılarının sayısını `rgguidSpecificEngines`.

 `pszStartPageUrl`

 [in] Otomatik-eklerken kullanılacak başlangıç URL'si.

 `pbstrSessionID`

 [out] Otomatik eklenen oturum kimliği.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür. Bir hata kodu `E_AUTO_ATTACH_NOT_REGISTERED`, auto-attach sınıf üreteci kaydedilmemiş gösterir.

## <a name="remarks"></a>Açıklamalar
 Belirtilen URL ile ilişkili bir program başladığında, belirtilen hata ayıklama motorlarını otomatik olarak başlatıldığını bağlı ve.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)