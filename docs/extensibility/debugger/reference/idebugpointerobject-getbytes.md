---
title: IDebugPointerObject::GetBytes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPointerObject::GetBytes
helpviewer_keywords:
- IDebugPointerObject::GetBytes method
ms.assetid: e986c188-87fb-4b51-86e9-ee6a0035bdab
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 25e18c189d40234773d9a9c2e219290d5fe9ba96
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53890819"
---
# <a name="idebugpointerobjectgetbytes"></a>IDebugPointerObject::GetBytes
Ardışık bir bayt serisi işaret ettiği değer alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetBytes(   
   DWORD  dwStart,  
   DWORD  dwCount,  
   BYTE*  pBytes,  
   DWORD* pdwBytes  
);  
```  
  
```csharp  
int GetBytes(  
   uint       dwStart,   
   uint       dwCount,   
   out byte[] pBytes,   
   out uint   pdwBytes  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwStart`  
 [in] Belirtilen nesnenin başından itibaren bayt cinsinden uzaklık.  
  
 `dwCount`  
 [in] Alınacak bayt sayısı.  
  
 `pBytes`  
 [out içinde] Değeri bir dizi ardışık bayt olarak doldurulan bir dizi nesnesinden belirtilen uzaklıkta başlayan işaret.  
  
 `pdwBytes`  
 [out] Gerçekte alınan bayt sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem kullanılır bu tarafından temsil edilen işaretçinin [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md) işaret türü basit tür veya basit bir dizi temel türlerin (diğer bir deyişle, basit bir bayt dizisi tarafından temsil edilen bir dizi).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPointerObject](../../../extensibility/debugger/reference/idebugpointerobject.md)   
 [SetBytes](../../../extensibility/debugger/reference/idebugpointerobject-setbytes.md)