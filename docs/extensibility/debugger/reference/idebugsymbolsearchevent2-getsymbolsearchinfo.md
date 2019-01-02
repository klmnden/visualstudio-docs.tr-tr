---
title: IDebugSymbolSearchEvent2::GetSymbolSearchInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
helpviewer_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
ms.assetid: ae9eb72b-f2aa-43b8-87ca-da19d2e78d17
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f02eba47963dc39e7fa1fc426a762ff9f30a664d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53888705"
---
# <a name="idebugsymbolsearchevent2getsymbolsearchinfo"></a>IDebugSymbolSearchEvent2::GetSymbolSearchInfo
Sembol yükleme işlemiyle ilgili sonuçları almak için bir olay işleyicisi olarak çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetSymbolSearchInfo(  
   IDebugModule3**    pModule,  
   BSTR*              pbstrDebugMessage,  
   MODULE_INFO_FLAGS* pdwModuleInfoFlags  
);  
```  
  
```csharp  
int GetSymbolSearchInfo(  
   IDebugModule3              pModule,   
   ref string                 pbstrDebugMessage,   
   out enum_MODULE_INFO_FLAGS pdwModuleInfoFlags  
);  
  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pModule`  
 [out] Bir IDebugModule3 simgeleri en iyi duruma yüklenen modül temsil eden nesne.  
  
 `pbstrDebugMessage`  
 [out içinde] Modülünden herhangi bir hata iletisi içeren bir dize döndürür. Hata yoksa bu dize yalnızca modülün adı içerir ancak hiçbir zaman boş değildir.  
  
> [!NOTE]
>  [C++] `pbstrDebugMessage` olamaz `NULL` ve ile serbest bırakılmalıdır `SysFreeString`.  
  
 `pdwModuleInfoFlags`  
 [out] Bayraklarının bir birleşimi [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md) simgeleri yüklenmiş olup olmadığını belirten sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir işleyici aldığında [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md) bir modül için hata ayıklama sembolleri için bir girişimde sonra olay işleyicisi Bu yük sonuçları belirlemek için bu yöntem çağırabilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)   
 [MODULE_INFO_FLAGS](../../../extensibility/debugger/reference/module-info-flags.md)   
 [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md)