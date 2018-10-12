---
title: IDebugReference2::GetDerivedMostReference | Microsoft Docs
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
- IDebugReference2::GetDerivedMostReference
helpviewer_keywords:
- IDebugReference2::GetDerivedMostReference
ms.assetid: 07253b74-7d39-48e0-8e85-ac8dfd919f6e
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 59c75dcc7994c9d5dd5f3f6ffa593df01bfbd97c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49278063"
---
# <a name="idebugreference2getderivedmostreference"></a>IDebugReference2::GetDerivedMostReference
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir başvuru türetilmiş çoğu referansını alır. Daha sonraki kullanımlar için ayrılmıştır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetDerivedMostReference(   
   IDebugReference2** ppDerivedMost  
);  
```  
  
```csharp  
int GetDerivedMostReference(   
   out IDebugReference2 ppDerivedMost  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppDerivedMost`  
 [out] Döndürür bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) türetilmiş çoğu özelliği temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Her zaman döndürür `E_NOTIMPL`.  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bu özelliği uygulayan bir nesne tanımlar `ClassRoot` ancak aslında örneklemesi olduğu `ClassDerived` sınıfından türetilen `ClassRoot`, sonra da bu yöntemi döndürür bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) nesnesi başvuruyu temsil eden `ClassDerived` nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)

