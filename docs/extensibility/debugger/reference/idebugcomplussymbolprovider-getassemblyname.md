---
title: IDebugComPlusSymbolProvider::GetAssemblyName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugComPlusSymbolProvider::GetAssemblyName
- GetAssemblyName
ms.assetid: a08cd609-b9b9-47bd-bf73-cbf851285907
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 59264db018b0098227abbcc44d8c697ffd57593d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948511"
---
# <a name="idebugcomplussymbolprovidergetassemblyname"></a>IDebugComPlusSymbolProvider::GetAssemblyName
Modül ve uygulama etki alanı belirtilen derlemenin adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
[C++]  
HRESULT GetAssemblyName(  
   ULONG32 ulAppDomainID,  
   GUID    guidModule,  
   BSTR*   pbstrName  
);  
```  
  
```  
[C#]  
int GetAssemblyName(  
   uint   ulAppDomainID,  
   Guid   guidModule,  
   string pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ulAppDomainID`  
 [in] Uygulama etki alanı için tanımlayıcı.  
  
 `guidModule`  
 [in] Modül için benzersiz tanımlayıcı.  
  
 `pbstrName`  
 [out] Derlemenin adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.  
  
```cpp  
HRESULT CDebugSymbolProvider::GetAssemblyName(  
    ULONG32 ulAppDomainID,  
    GUID guidModule,  
    BSTR* pbstrName  
)  
{  
    HRESULT hr = S_OK;  
    Module_ID idModule(ulAppDomainID, guidModule);  
    CComPtr<IMetaDataImport> pMetadata;  
  
    METHOD_ENTRY( CDebugSymbolProvider::GetMetadataForModule );  
  
    IfFalseGo( pbstrName, E_INVALIDARG );  
    *pbstrName = NULL;  
  
    IfFailGo( GetMetadata( idModule, &pMetadata ) );  
    IfFailGo( GetAssemblyName( pMetadata, 0, pbstrName ) );  
  
Error:  
  
    METHOD_EXIT( CDebugSymbolProvider::GetMetadataForModule, hr );  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)