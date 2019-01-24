---
title: IDebugSymbolProviderDirect::GetMetaDataImport | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- GetMetaDataImport
- IDebugSymbolProviderDirect::GetMetaDataImport
ms.assetid: b51a492c-af00-4b08-93fb-6c19ee4916aa
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 738169ece185bfc4b861b8f8220199dbf3c762b1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54768718"
---
# <a name="idebugsymbolproviderdirectgetmetadataimport"></a>IDebugSymbolProviderDirect::GetMetaDataImport
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Meta veri alma bilgilerini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetMetaDataImport (  
    GUID*      guid,  
    DWORD      appID,  
    IUnknown** ppImport  
);  
```  
  
```csharp  
int GetMetaDataImport (  
    Guid       guid,  
    uint       appID,  
    out object ppImport  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guid`  
 [in] Modül için benzersiz tanımlayıcı.  
  
 `appID`  
 [in] Uygulama etki alanı için tanımlayıcı.  
  
 `ppImport`  
 [out] Bir meta veriler içeren bir nesne döndürür, bilgi alın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProviderDirect](../../../extensibility/debugger/reference/idebugsymbolproviderdirect.md)
