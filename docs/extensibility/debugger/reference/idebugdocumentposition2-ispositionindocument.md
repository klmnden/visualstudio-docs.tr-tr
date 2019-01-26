---
title: IDebugDocumentPosition2::IsPositionInDocument | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: 7bb112a19c933cdcdf3cc2f9e127ab2c06127bf0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54965360"
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
 [IDebugDocumentPosition2](../../../extensibility/debugger/reference/idebugdocumentposition2.md)   
 [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)