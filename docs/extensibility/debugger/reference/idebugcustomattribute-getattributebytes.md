---
title: IDebugCustomAttribute::GetAttributeBytes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCustomAttribute::GetAttributeBytes
helpviewer_keywords:
- IDebugCustomAttribute::GetAttributeBytes
ms.assetid: cf34583b-6530-4dcc-89f8-eb27e4e8d594
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: b892f6b12937c4cd68d718a3dc7e6d957ad1325d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53913139"
---
# <a name="idebugcustomattributegetattributebytes"></a>IDebugCustomAttribute::GetAttributeBytes
Bir blobu bayt olarak öznitelik bilgileri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetAttributeBytes(   
   BYTE*  ppBlob,  
   DWORD* pdwLen  
);  
```  
  
```csharp  
int GetAttributeBytes(  
   ref byte[] ppBlob,   
   ref uint   pdwLen  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppBlob`  
 [out içinde] Öznitelik bayt ile doldurulmuş bir dizi.  
  
 `pdwLen`  
 [out içinde] Bayt olarak döndürülecek en fazla sayısını belirtir `ppBlob` dizisi ve diziye gerçekte yazılan bayt sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Ayarlama `ppBlob` kullanılabilir bayt sayısını döndürmek için bir null değer parametresi öznitelikleri. Ardından bir dizi ayırmak ve geçirmek için bu dizide `ppBlob` parametresi.  
  
 Öznitelik bayt özel özniteliğinin ham verileri temsil eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)