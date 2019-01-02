---
title: IDebugDocumentContext2::Seek | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDocumentContext2::Seek
helpviewer_keywords:
- IDebugDocumentContext2::Seek
ms.assetid: 71501356-8a82-4d36-b354-6625bdd2baa0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: db5c44d79882d887e8a852f3add491317dbf96fa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53895532"
---
# <a name="idebugdocumentcontext2seek"></a>IDebugDocumentContext2::Seek
Belge bağlamı belirli sayıda deyimleri veya satırları tarafından taşır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Seek(   
   int                      nCount,  
   IDebugDocumentContext2** ppDocContext  
);  
```  
  
```cpp  
int Seek(   
   int                        nCount,  
   out IDebugDocumentContext2 ppDocContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `nCount`  
 [in] Deyimleri ya da isterseniz, belge bağlamına bağlı olarak taşımak için satır sayısı.  
  
 `ppDocContext`  
 [out] Yeni bir [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) yeni konum nesnesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)