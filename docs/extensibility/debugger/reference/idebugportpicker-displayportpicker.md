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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 00923556927f2fed7e5895df2db391a45463e57e
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212902"
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

## <a name="parameters"></a>Parametreler
`hwndParentDialog`\
[in] Üst iletişim kutusu için tanıtıcı.

`pbstrPortId`\
[out] Bağlantı noktası tanımlayıcı dizesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Dönüş değeri `S_FALSE` (ya da dönüş değeri `S_OK` ile `BSTR` kümesine `NULL`) kullanıcının tıkladığını belirtir **iptal**.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)