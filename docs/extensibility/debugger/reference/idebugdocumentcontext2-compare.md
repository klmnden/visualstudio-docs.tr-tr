---
title: IDebugDocumentContext2::Compare | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDocumentContext2::Compare
helpviewer_keywords:
- IDebugDocumentContext2::Compare
ms.assetid: 2327b1ba-52d0-42fb-a01e-63cb4b332d2f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3a4475dd8031dd75a35dda8950b8005886ec9b47
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53866705"
---
# <a name="idebugdocumentcontext2compare"></a>IDebugDocumentContext2::Compare
Bu belge bağlamları belirli bir dizi belge bağlamına karşılaştırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Compare(   
   DOCCONTEXT_COMPARE       compare,  
   IDebugDocumentContext2** rgpDocContextSet,  
   DWORD                    dwDocContextSetLen,  
   DWORD*                   pdwDocContext  
);  
```  
  
```csharp  
int Compare(   
   enum_ DOCCONTEXT_COMPARE compare,  
   IDebugDocumentContext2[] rgpDocContextSet,  
   uint                     dwDocContextSetLen,  
   out uint                 pdwDocContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `compare`  
 [in] Bir değer [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md) karşılaştırma türünü belirten sabit listesi.  
  
 `rgpDocContextSet`  
 [in] Bir dizi [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) karşılaştırılan belge bağlamı temsil eden nesneleri.  
  
 `dwDocContextSetLen`  
 [in] Karşılaştırılacak belge bağlamları dizinin uzunluğu.  
  
 `pdwDocContext`  
 [out] Dizine döndürür `rgpDocContextSet` karşılaştırmayı ilk belge bağlamı dizisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` bir eşleşme bulunmazsa. Döndürür `S_FALSE` eşleşme bulunmazsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) uygulayan aynı hata ayıklama altyapısı tarafından dizide geçirilen nesneleri uygulanan `IDebugDocumentContext2` üzerinde; Aksi takdirde, çağrılan nesne karşılaştırma geçerli değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md)