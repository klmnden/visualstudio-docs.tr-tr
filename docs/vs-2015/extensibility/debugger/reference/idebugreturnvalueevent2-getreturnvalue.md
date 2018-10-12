---
title: IDebugReturnValueEvent2::GetReturnValue | Microsoft Docs
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
- IDebugReturnValueEvent2::GetReturnValue
helpviewer_keywords:
- IDebugReturnValueEvent2::GetReturnValue
ms.assetid: 86c50d5a-6df6-4798-818a-c587a8741f90
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 40b92e7145a91cd0d73acd437adc232f44df9d37
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49273474"
---
# <a name="idebugreturnvalueevent2getreturnvalue"></a>IDebugReturnValueEvent2::GetReturnValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Şirket dışı veya bir işlevin üzerinden Adımlama döndürülen değer alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetReturnValue (   
   IDebugProperty2** ppReturnValue  
);  
```  
  
```csharp  
int GetReturnValue (   
   out IDebugProperty2 ppReturnValue  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppReturnValue`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) alınacak değerini temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugReturnValueEvent2](../../../extensibility/debugger/reference/idebugreturnvalueevent2.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)

