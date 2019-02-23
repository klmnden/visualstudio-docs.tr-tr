---
title: IDebugDocumentPosition2::IsPositionInDocument | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentPosition2::IsPositionInDocument
helpviewer_keywords:
- IDebugDocumentPosition2::IsPositionInDocument
ms.assetid: d5cf57cb-b93b-4e1d-bec9-185f4fe8668d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e5701df9085de7a63e7f09ea37c28244897122b7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678924"
---
# <a name="idebugdocumentposition2ispositionindocument"></a>IDebugDocumentPosition2::IsPositionInDocument
Belge konumu verilen belgedeki dahil olup olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsPositionInDocument( 
   IDebugDocument2* pDoc
);
```

```csharp
int IsPositionInDocument( 
   IDebugDocument2 pDoc
);
```

#### <a name="parameters"></a>Parametreler
 `pDoc`

 [in] [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) içeren belge aday temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem öncelikle kesme noktası ayarlanırken kullanılan [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md) arabirimleri. Belgeler yüklenen gibi kesme noktası konumu belge bu konuma içerip içermediğini belirlemek için çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md)
- [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)