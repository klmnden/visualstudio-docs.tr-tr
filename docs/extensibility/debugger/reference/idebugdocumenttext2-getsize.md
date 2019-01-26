---
title: IDebugDocumentText2::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDocumentText2::GetSize
helpviewer_keywords:
- IDebugDocumentText2::GetSize
ms.assetid: bf515a8f-dcee-4004-8f81-543d547ceaae
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b22ed5f7f99e8a0e7a5f3a2d55b98de7dcd781bc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54932993"
---
# <a name="idebugdocumenttext2getsize"></a>IDebugDocumentText2::GetSize
Belgedeki bu konumda metin boyutunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetSize(   
   ULONG* pcNumLines,  
   ULONG* pcNumChars  
);  
```  
  
```csharp  
int GetSize(   
   ref uint pcNumLines,  
   ref uint pcNumChars  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcNumLines`  
 [out] Metin satırlarını döndürür.  
  
 `pcNumChars`  
 [out] Metin karakter sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [Yalnızca C++] Belirli bir değeri istenildiği gibi değilse, parametre için NULL geçirin.  
  
 [C# yalnızca] Her iki parametre belirtilmelidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentText2](../../../extensibility/debugger/reference/idebugdocumenttext2.md)