---
title: IDebugDocumentContext2::GetSourceRange | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDocumentContext2::GetSourceRange
helpviewer_keywords:
- IDebugDocumentContext2::GetSourceRange
ms.assetid: 5903c75e-5390-4d13-9314-1ee276255313
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: bcec6af2b8e7b1acfdc9c3cf38cb18654be78c53
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68145008"
---
# <a name="idebugdocumentcontext2getsourcerange"></a>IDebugDocumentContext2::GetSourceRange
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu belge bağlamına kaynak kod aralığını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetSourceRange(   
   TEXT_POSITION* pBegPosition,  
   TEXT_POSITION* pEndPosition  
);  
```  
  
```csharp  
int GetSourceRange(   
   TEXT_POSITION[] pBegPosition,  
   TEXT_POSITION[] pEndPosition  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pBegPosition`  
 [out içinde] A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) başlangıç konumu ile doldurulmuş yapısı. Bu bilgiler gerekli değildir, bu bağımsız değişken null bir değere ayarlayın.  
  
 `pEndPosition`  
 [out içinde] A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) oturum bitiş konumu girilir yapısının. Bu bilgiler gerekli değildir, bu bağımsız değişken null bir değere ayarlayın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir kaynak aralıktaki tüm kaynak koddan kod katkıda önceki deyiminden sonra yalnızca geçerli deyim arka aralığıdır. Kaynak aralığı genellikle Ayrıştırılmış kod penceresinde kodu, Yorumlar dahil olmak üzere kaynak deyimlerini karıştırmak için kullanılır.  
  
 Yalnızca bu belge bağlamı içinde yer alan kod deyimlerini aralığı almak için arama [GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [GetStatementRange](../../../extensibility/debugger/reference/idebugdocumentcontext2-getstatementrange.md)   
 [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)
