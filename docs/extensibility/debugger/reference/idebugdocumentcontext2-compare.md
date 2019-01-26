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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 06fe3b1c2acffa47f7c47f5f9426fb1d07bbf288
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54937840"
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