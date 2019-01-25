---
title: IDebugDocumentPosition2::IsPositionInDocument | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDocumentPosition2::IsPositionInDocument
helpviewer_keywords:
- IDebugDocumentPosition2::IsPositionInDocument
ms.assetid: d5cf57cb-b93b-4e1d-bec9-185f4fe8668d
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7950f091d34d03222044455be671e15f5297a747
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54796200"
---
# <a name="idebugdocumentposition2ispositionindocument"></a>IDebugDocumentPosition2::IsPositionInDocument
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belge konumu verilen belgedeki dahil olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
