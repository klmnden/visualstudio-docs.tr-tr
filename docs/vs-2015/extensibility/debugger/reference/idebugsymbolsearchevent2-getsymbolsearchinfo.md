---
title: IDebugSymbolSearchEvent2::GetSymbolSearchInfo | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
helpviewer_keywords:
- IDebugSymbolSearchEvent2::GetSymbolSearchInfo
ms.assetid: ae9eb72b-f2aa-43b8-87ca-da19d2e78d17
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c8ef097ed02ae90b03289e3a2f3a1ad3f0ad8618
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446046"
---
# <a name="idebugsymbolsearchevent2getsymbolsearchinfo"></a>IDebugSymbolSearchEvent2::GetSymbolSearchInfo
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

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
> [C++] `pbstrDebugMessage` olamaz `NULL` ve ile serbest bırakılmalıdır `SysFreeString`.  
  
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
