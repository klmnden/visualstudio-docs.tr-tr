---
title: IDebugProperty3::GetStringChars | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProperty3::GetStringChars
helpviewer_keywords:
- IDebugProperty3::GetStringChars
ms.assetid: 832c37f3-85cb-4227-8ab2-f27a80eafe90
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0737607a8905e96e02b7189761198a7e9e3915b6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54768154"
---
# <a name="idebugproperty3getstringchars"></a>IDebugProperty3::GetStringChars
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu özellik ile ilişkili dizeyi alır ve bir kullanıcı tarafından sağlanan arabelleğinde depolar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetStringChars(  
   ULONG  buflen,  
   WCHAR* rgString,  
   ULONG* pceltFetched  
);  
```  
  
```csharp  
int GetStringChars(  
   uint       buflen,   
   out string rgString,   
   out uint   pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `buflen`  
 [in] En fazla karakter sayısı, kullanıcı tarafından sağlanan arabellek barındırabilir.  
  
 `rgString`  
 [out] Bir dize döndürür.  
  
 [C++ yalnızca] `rgString` Unicode karakter dizesinin alan arabellek işaretçisidir. Bu arabelleğin en az olmalıdır `buflen` boyutu (bayt değil) karakter.  
  
 `pceltFetched`  
 [out] Burada aslında arabellekteki depolanan karakter sayısı döndürülür. (Olabilir `NULL` c++.)  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 C++'da, arabelleğin en az olduğunu sağlamak üzere dikkatli olunması gerekir `buflen` Unicode karakter uzunluğuna sahip. Bir Unicode karakter 2 bayt uzunluğunda olduğunu unutmayın.  
  
> [!NOTE]
>  C++'da, döndürülen dizeye Sonlandırıcı null karakterini içermez. Verilen `pceltFetched` dizedeki karakter sayısını belirtir.  
  
## <a name="example"></a>Örnek  
<!-- TODO: review snippet reference  [!CODE [[cpp]]([cpp])]  -->  
  
```  
CStringW RetrievePropertyString(IDebugProperty2 *pPropInfo)  
{  
    CStringW returnString = L"";  
    CComQIPtr<IDebugProperty3> pProp3 = pPropInfo->pProperty;  
    If (pProp3 != NULL) {  
        ULONG dwStrLen = 0;  
        HRESULT hr;  
        hr = pProp3->GetStringCharLength(&dwStrLen);  
        if (SUCCEEDED(hr) && dwStrLen > 0) {  
            ULONG dwRead;  
            CStrBufW buf(returnString,dwStrLen,CStrBuf::SET_LENGTH);  
            hr = pProp3->GetStringChars(dwStrLen,  
                                        reinterpret_cast<WCHAR*>(static_cast<CStringW::PXSTR>(buf)),  
                                        &dwRead);  
        }  
    }  
    return(returnString);  
```  
  
<!-- TODO: review snippet reference  [!CODE [}](})]  -->  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetStringCharLength](../../../extensibility/debugger/reference/idebugproperty3-getstringcharlength.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)