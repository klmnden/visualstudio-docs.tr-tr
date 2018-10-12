---
title: IDebugSymbolProvider::GetAddressesFromContext | Microsoft Docs
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
- IDebugSymbolProvider::GetAddressesFromContext
helpviewer_keywords:
- IDebugSymbolProvider::GetAddressesFromContext method
ms.assetid: a3124883-a255-4543-a5ec-e1c7a97beb69
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 51b9259473d186879e6d9961fdedc15b8f22b110
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49294287"
---
# <a name="idebugsymbolprovidergetaddressesfromcontext"></a>IDebugSymbolProvider::GetAddressesFromContext
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, bir belge bağlamına bir hata ayıklama adresleri dizisine eşler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetAddressesFromContext(   
   IDebugDocumentContext2* pDocContext,  
   BOOL                    fStatmentOnly,  
   IEnumDebugAddresses**   ppEnumBegAddresses,  
   IEnumDebugAddresses**   ppEnumEndAddresses  
);  
```  
  
```csharp  
int GetAddressesFromContext(  
   IDebugDocumentContext2  pDocContext,  
   bool                    fStatmentOnly,  
   out IEnumDebugAddresses ppEnumBegAddresses,  
   out IEnumDebugAddresses ppEnumEndAddresses  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pDocContext`  
 [in] Belge bağlamı.  
  
 `fStatmentOnly`  
 [in] TRUE ise tek bir deyimde hata ayıklama adresler sınırlar.  
  
 `ppEnumBegAddresses`  
 [out] Bu deyim veya satır ile ilişkili başlangıç hata ayıklama adresi için bir numaralandırıcı döndürür.  
  
 `ppEnumEndAddresses`  
 [out] Döndürür bir [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md) bu deyimi veya satır ile ilişkili bitiş hata ayıklama adresi için bir numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir belge bağlamına genellikle bir dizi kaynak satırları gösterir. Bu yöntem, başlangıç sağlar ve bitiş adreslerini hata ayıklama bu satırlar ile ilişkili. Bazı diller, birden fazla satır ya da birden fazla deyim içeren satırları span deyimleri sağlar. Bu yöntem, tek bir deyimde hata ayıklama adresler sınırlamak için bir bayrak sağlar.  
  
 Tek bir deyimde şablonları olduğu gibi birden çok hata ayıklama adresi olması mümkündür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)   
 [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md)

