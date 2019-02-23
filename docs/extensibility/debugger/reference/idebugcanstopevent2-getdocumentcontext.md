---
title: IDebugCanStopEvent2::GetDocumentContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2::GetDocumentContext
helpviewer_keywords:
- IDebugCanStopEvent2::GetDocumentContext
ms.assetid: 936a6c4e-30c5-4c7e-9ad5-910cc605a4b5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2066d712824ec40c822a813eb20a6afffd7981ab
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56721036"
---
# <a name="idebugcanstopevent2getdocumentcontext"></a>IDebugCanStopEvent2::GetDocumentContext
Bu olay konumunu tanımlayan belge bağlamını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDocumentContext ( 
   IDebugDocumentContext2** ppDocCxt
);
```

```csharp
int GetDocumentContext ( 
   out IDebugDocumentContext2 ppDocCxt
);
```

#### <a name="parameters"></a>Parametreler
 `ppDocCxt`

 [out] Döndürür [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) geçerli kod konumuna karşılık gelen bir kaynak dosyası belgedeki bir konumu temsil eden arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Genellikle, belge bağlamı, kaynak dosyada bir konum olarak düşünülebilir.

 Kod yönergeler yönlendirilmiş olan kod bağlamı alma çağrısı [GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)
- [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)
- [GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md)