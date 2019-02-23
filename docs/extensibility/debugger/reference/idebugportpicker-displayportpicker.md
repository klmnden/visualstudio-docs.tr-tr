---
title: IDebugPortPicker::DisplayPortPicker | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- DisplayPortPicker
- IDebugPortPicker::DisplayPortPicker
ms.assetid: 08511ef5-be64-4069-b169-a569cc94bc64
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8e115c4e45784b2072bf626d90ebab0d980491e4
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687360"
---
# <a name="idebugportpickerdisplayportpicker"></a>IDebugPortPicker::DisplayPortPicker
Kullanıcının bir bağlantı noktası seçmesine izin veren belirtilen iletişim kutusunu görüntüler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT DisplayPortPicker(
   HWND hwndParentDialog,
   BSTR* pbstrPortId
);
```

```csharp
public int DisplayPortPicker(
   int hwndParentDialog,
   out string pbstrPortId
);
```

#### <a name="parameters"></a>Parametreler
 `hwndParentDialog`

 [in] Üst iletişim kutusu için tanıtıcı.

 `pbstrPortId`

 [out] Bağlantı noktası tanımlayıcı dizesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş değeri `S_FALSE` (ya da dönüş değeri `S_OK` ile `BSTR` kümesine `NULL`) kullanıcının tıkladığını belirtir **iptal**.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)