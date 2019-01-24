---
title: IDebugDisassemblyStream2::GetCodeLocationId | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
helpviewer_keywords:
- IDebugDisassemblyStream2::GetCodeLocationId
ms.assetid: 567adfb8-2f54-499a-a027-e4ecb82277ef
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ebb2280f814985e2352413921a00268d96761b7d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54785021"
---
# <a name="idebugdisassemblystream2getcodelocationid"></a>IDebugDisassemblyStream2::GetCodeLocationId
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirli kod bağlamı için bir kod konum tanımlayıcısı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
