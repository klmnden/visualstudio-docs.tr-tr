---
title: IDebugSymbolProvider::GetLanguage | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugSymbolProvider::GetLanguage
helpviewer_keywords:
- IDebugSymbolProvider::GetLanguage method
ms.assetid: e4142183-3d8b-418f-907f-4ee4c753d8ce
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 130cfc1a0b1e594deb460839162dd3d68cb5f525
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49280247"
---
# <a name="idebugsymbolprovidergetlanguage"></a>IDebugSymbolProvider::GetLanguage
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, hata ayıklama adresten Kodu derlemek için kullanılan dili alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetLanguage(   
   IDebugAddress* pAddress,  
   GUID*          pguidLanguage,  
   GUID*          pguidLanguageVendor  
);  
```  
  
```csharp  
int GetLanguage(  
   IDebugAddress pAddress,   
   out Guid      pguidLanguage,   
   out Guid      pguidLanguageVendor  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pAddress`  
 [in] Bir adres nesnesini temsil ettiği bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.  
  
 `pguidLanguage`  
 [out] Döndürür bir `GUID` dili belirtir.  
  
 `pguidLanguageVendor`  
 [out] Döndürür bir `GUID` dil satıcı belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı, doğru bir ifade değerlendiricisi seçmek gereken bilgileri elde etmek için bu yöntemi çağırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)

