---
title: CONTEXT_INFO | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- CONTEXT_INFO
helpviewer_keywords:
- CONTEXT_INFO structure
ms.assetid: 6b513f4e-e7b0-4969-adf0-2205ccc1e09b
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: f4e8c1b438cd2fa2721e81f055695e5836c26d12
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68179946"
---
# <a name="contextinfo"></a>CONTEXT_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı, bellek bağlamı veya kod bağlamı açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct _tagCONTEXT_INFO {   
   CONTEXT_INFO_FIELDS dwFields;  
   BSTR                bstrModuleUrl;  
   BSTR                bstrFunction;  
   TEXT_POSITION       posFunctionOffset;  
   BSTR                bstrAddress;  
   BSTR                bstrAddressOffset;  
   BSTR                bstrAddressAbsolute;  
} CONTEXT_INFO;  
```  
  
```csharp  
public struct CONTEXT_INFO {  
   public uint          dwFields;  
   public string        bstrModuleUrl;  
   public string        bstrFunction;  
   public TEXT_POSITION posFunctionOffset;  
   public string        bstrAddress;  
   public string        bstrAddressOffset;  
   public string        bstrAddressAbsolute;  
};  
```  
  
## <a name="members"></a>Üyeler  
 dwFields  
 He bayraklarının bir birleşimi [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md) hangi alanların doldurulmuş belirten numaralandırma<strong>.</strong>  
  
 bstrModuleUrl  
 Bağlam bulunduğu modülünün adı.  
  
 bstrFunction  
 Bağlam bulunduğu işlevi adı.  
  
 posFunctionOffset  
 A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) kod bağlamı ile ilişkili işlevi satır ve sütun uzaklığı tanımlayan yapısı.  
  
 bstrAddress  
 Belirtilen bağlamda bulunduğu kod adresi.  
  
 bstrAddressOffset  
 Belirtilen bağlamda bulunduğu kod adres uzaklığı.  
  
 bstrAddressAbsolute  
 Belirtilen bağlamda bulunduğu bellek mutlak bir adres.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı çağrısından döndürülen [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md) yöntemi.  
  
 Bu yapı için genel kullanım support biri olan bir **bellek** hata ayıklama penceresine.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md)   
 [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md)   
 [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)
