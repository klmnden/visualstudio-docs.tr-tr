---
title: IDebugCustomAttributeQuery2::EnumCustomAttributes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCustomAttributeQuery2::EnumCustomAttributes
helpviewer_keywords:
- IDebugCustomAttributeQuery2::EnumCustomAttributes
ms.assetid: 94bfce74-aa3d-45f0-8e04-5715faf85217
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 25dec8aa273d9b5fa89ce557d95cac181f2fe6de
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53929858"
---
# <a name="idebugcustomattributequery2enumcustomattributes"></a>IDebugCustomAttributeQuery2::EnumCustomAttributes
Bu alana ekli tüm özel öznitelikleri için bir numaralandırıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumCustomAttributes(   
   IEnumDebugCustomAttributes** ppEnum  
);  
```  
  
```csharp  
int EnumCustomAttributes(  
   out IEnumDebugCustomAttributes ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md) özel öznitelik listesini temsil eden nesne; Aksi takdirde, özel öznitelik yoksa null değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu alan özel öznitelik yoksa başarılıysa S_OK veya S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür;  
  
## <a name="remarks"></a>Açıklamalar  
 Bir alan birden çok özel özniteliklere sahip olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCustomAttributeQuery2](../../../extensibility/debugger/reference/idebugcustomattributequery2.md)   
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)