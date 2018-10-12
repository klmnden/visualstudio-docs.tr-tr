---
title: IDebugSymbolProviderDirect::GetMethodFromAddress | Microsoft Docs
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
- IDebugSymbolProviderDirect::GetMethodFromAddress
- GetMethodFromAddress
ms.assetid: 33ffd197-1221-41bc-a9f6-f133ebdcb783
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: beb33d3ca8898f5f57f94ec3cb23bbb5f49fa7d9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49183800"
---
# <a name="idebugsymbolproviderdirectgetmethodfromaddress"></a>IDebugSymbolProviderDirect::GetMethodFromAddress
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirtilen hata ayıklama adresindeki yöntem hakkında bilgi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetMethodFromAddress(  
   IDebugAddress* pAddress,  
   GUID*          pGuid,  
   DWORD*         pAppID,  
   _mdToken*      pTokenClass,  
   _mdToken*      pTokenMethod,  
   DWORD*         pdwOffset,  
   DWORD*         pdwVersion  
);  
```  
  
```csharp  
int GetMethodFromAddress(  
   IDebugAddress pAddress,  
   out Guid      pGuid,  
   out uint      pAppID,  
   out uint      pTokenClass,  
   out uint      pTokenMethod,  
   out uint      pdwOffset,  
   out uint      pdwVersion  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pAddress`  
 [in] Tarafından temsil edilen adresi hata ayıklama [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.  
  
 `pGuid`  
 [out] Modülün benzersiz tanımlayıcısı.  
  
 `pAppID`  
 [out] Uygulama etki alanı tanımlayıcısı.  
  
 `pTokenClass`  
 [out] Belirteç, içeren sınıfı temsil eder.  
  
 `pTokenMethod`  
 [out] Modülü temsil eden belirteç.  
  
 `pdwOffset`  
 [out] Başından itibaren bayt uzaklığını `pAddress` parametresi.  
  
 `pdwVersion`  
 [out] Yöntem sürüm numarası.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProviderDirect](../../../extensibility/debugger/reference/idebugsymbolproviderdirect.md)

