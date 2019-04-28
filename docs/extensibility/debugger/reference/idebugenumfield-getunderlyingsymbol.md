---
title: IDebugEnumField::GetUnderlyingSymbol | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetUnderlyingSymbol
helpviewer_keywords:
- IDebugEnumField::GetUnderlyingSymbol method
ms.assetid: c3b8a117-6708-4cfd-8ffc-5f007d706bc5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9b6b90f388f93bc7cfc2c246c529217bcdb00fa9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62920270"
---
# <a name="idebugenumfieldgetunderlyingsymbol"></a>IDebugEnumField::GetUnderlyingSymbol
Bu yöntem döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) , numaralandırma adını temsil eder.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetUnderlyingSymbol(
   IDebugField** ppField
);
```

```csharp
int GetUnderlyingSymbol(
   out IDebugField ppField
);
```

#### <a name="parameters"></a>Parametreler
 `ppField`

 [out] Döndürür [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) açıklayan bu sabit listesi adı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Numaralandırma adını kullanarak bir bellek konumuna bağlı sabit listesi türü de içeren [bağlama](../../../extensibility/debugger/reference/idebugbinder-bind.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)