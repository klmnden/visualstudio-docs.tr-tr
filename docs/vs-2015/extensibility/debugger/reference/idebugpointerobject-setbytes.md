---
title: IDebugPointerObject::SetBytes | Microsoft Docs
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
- IDebugPointerObject::SetBytes
helpviewer_keywords:
- IDebugPointerObject::SetBytes method
ms.assetid: 8c578b38-38d7-46f3-bb2e-8a730fccd334
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2358ea408edea5803fb7726e21d292400c083bdb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49226297"
---
# <a name="idebugpointerobjectsetbytes"></a>IDebugPointerObject::SetBytes
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Art arda bayt dizisinden işaret değeri ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT SetBytes(   
   DWORD  dwStart,  
   DWORD  dwCount,  
   BYTE*  pBytes,  
   DWORD* pdwBytes  
);  
```  
  
```csharp  
int SetBytes(  
   uint     dwStart,   
   uint     dwCount,   
   byte[]   pBytes,   
   out uint pdwBytes  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwStart`  
 [in] Belirtilen nesnenin başından itibaren bayt cinsinden uzaklık.  
  
 `dwCount`  
 [in] Ayarlanacak bayt sayısı.  
  
 `pBytes`  
 [in] Yeni değeri temsil eden bir bayt dizisi. Bu değer, belirtilen uzaklıkta başlayan belirli nesne içinde depolanır.  
  
 `pdwBytes`  
 [out] Bayt sayısı gerçekte ayarlamak döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem kullanılır bu tarafından temsil edilen işaretçinin [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md) işaret türü basit tür veya basit bir dizi temel türlerin (diğer bir deyişle, basit bir bayt dizisi tarafından temsil edilen bir dizi). Bu `IDebugPointerObject` nesne (onu işaret etmelidir bir bellek adresi) bir null başvuru olamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetBytes](../../../extensibility/debugger/reference/idebugpointerobject-getbytes.md)   
 [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)

