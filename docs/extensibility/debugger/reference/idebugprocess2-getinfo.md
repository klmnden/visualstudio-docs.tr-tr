---
title: IDebugProcess2::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::GetInfo
helpviewer_keywords:
- IDebugProcess2::GetInfo
ms.assetid: 46021dce-bb97-46c3-b0cc-e5b3b68acc35
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e6227e8a4397dac03e9ecc70eedf2b902888cdbb
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353148"
---
# <a name="idebugprocess2getinfo"></a>IDebugProcess2::GetInfo
İşlemin bir açıklamasını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetInfo(
   PROCESS_INFO_FIELDS  Fields,
   PROCESS_INFO*        pProcessInfo
);
```

```csharp
int GetInfo(
   enum_PROCESS_INFO_FIELDS  Fields,
   PROCESS_INFO[]            pProcessInfo
);
```

## <a name="parameters"></a>Parametreler
`Fields`\
[in] Değerleri birleşimi [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md) hangi alanları belirten numaralandırma `pProcessInfo` parametresi olan doldurulmalıdır.

`pProcessInfo`\
[out] A [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) işlemin bir açıklamasını oturum doldurulmuş yapısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md)
- [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)