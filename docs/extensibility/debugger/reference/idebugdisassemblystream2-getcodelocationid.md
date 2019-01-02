---
title: IDebugDisassemblyStream2::GetCodeLocationId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
helpviewer_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
ms.assetid: 567adfb8-2f54-499a-a027-e4ecb82277ef
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 52423c671bb27de0c5b03a302dc757cad7a3aaa1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891524"
---
# <a name="idebugdisassemblystream2getcodelocationid"></a>IDebugDisassemblyStream2::GetCodeLocationId
Belirli kod bağlamı için bir kod konum tanımlayıcısı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetCodeLocationId(   
   IDebugCodeContext2* pCodeContext,  
   UINT64*             puCodeLocationId  
);  
```  
  
```csharp  
int GetCodeLocationId(   
   IDebugCodeContext2 pCodeContext,  
   out ulong          puCodeLocationId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCodeContext`  
 [in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) tanımlayıcıya dönüştürülecek nesne.  
  
 `puCodeLocationId`  
 [out] Kod konumu tanımlayıcısını döndürür. Açıklamalara bakın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_CODE_CONTEXT_OUT_OF_SCOPE` kod bağlamı geçerli olup olmadığını ancak kapsamı dışında.  
  
## <a name="remarks"></a>Açıklamalar  
 Ayrıştırılmış kodu destekleyen hata ayıklama altyapısına (DE) kod konum tanımlayıcısı özeldir. Bu konum tanımlayıcısı kod konumda izlemek için DE tarafından dahili olarak kullanılır ve genellikle bir adresi veya bir tür uzaklığı. Bir konum kod bağlamı başka bir konum kod bağlamı altındaysa ilk kod bağlamı karşılık gelen kod konum tanımlayıcısı de ikinci kod bağlamı kod konum tanımlayıcısı değerinden küçük olmalıdır tek gereksinim olmasıdır.  
  
 Bir kod konum tanımlayıcısı kod bağlamı almak için arama [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [GetCodeContext](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext.md)