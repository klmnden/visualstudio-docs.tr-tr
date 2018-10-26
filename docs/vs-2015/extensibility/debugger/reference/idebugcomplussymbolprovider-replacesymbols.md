---
title: IDebugComPlusSymbolProvider::ReplaceSymbols | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- ReplaceSymbols
- IDebugComPlusSymbolProvider::ReplaceSymbols
ms.assetid: 82fbc8db-c4b1-432f-bec9-1a9dc09570be
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 88a47336c76ca785a3fee0c5110580476d27f3da
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49855345"
---
# <a name="idebugcomplussymbolproviderreplacesymbols"></a>IDebugComPlusSymbolProvider::ReplaceSymbols
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Geçerli hata ayıklama sembolleri, belirtilen veri akışında değerlerle değiştirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT ReplaceSymbols(  
   ULONG32  ulAppDomainID,  
   GUID     guidModule,  
   IStream* pStream  
);  
```  
  
```csharp  
int ReplaceSymbols(  
   uint    ulAppDomainID,  
   Guid    guidModule,  
   IStream pStream  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ulAppDomainID`  
 [in] Uygulama etki alanı tanımlayıcısı.  
  
 `guidModule`  
 [in] Modülün benzersiz tanımlayıcısı.  
  
 `pStream`  
 [in] Yeni semboller içeren veri akışı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek için bu yöntemi uygulaması gösterilmiştir bir **CDebugSymbolProvider** gösteren nesne [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) arabirimi.  
  
```cpp#  
HRESULT CDebugSymbolProvider::ReplaceSymbols(  
    ULONG32 ulAppDomainID,  
    GUID guidModule,  
    IStream* pStream  
)  
{  
    HRESULT hr = S_OK;  
    CComPtr<CModule> pModule;  
    Module_ID idModule(ulAppDomainID, guidModule);  
  
    METHOD_ENTRY( CDebugSymbolProvider::ReplaceSymbols );  
  
    IfFailGo( GetModule( idModule, &pModule ) );  
    IfFailGo( pModule->ReplaceSymbols( pStream ) );  
  
Error:  
  
    METHOD_EXIT( CDebugSymbolProvider::ReplaceSymbols, hr );  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)

