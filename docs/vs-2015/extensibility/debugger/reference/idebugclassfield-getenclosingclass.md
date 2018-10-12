---
title: IDebugClassField::GetEnclosingClass | Microsoft Docs
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
- IDebugClassField::GetEnclosingClass
helpviewer_keywords:
- IDebugClassField::GetEnclosingClass method
ms.assetid: a0c12e3c-9ea0-4dfb-9e45-8cea18725022
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 7ebbfcfbd0fc8d21dfc67193e6e1164e38c923dc
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49225509"
---
# <a name="idebugclassfieldgetenclosingclass"></a>IDebugClassField::GetEnclosingClass
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu sınıfın kapsayan sınıf alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetEnclosingClass(   
   IDebugClassField** ppClassField  
);  
```  
  
```csharp  
int GetEnclosingClass(  
   out IDebugClassField ppClassField  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppClassField`  
 [out] Döndürür bir [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) sınıfı kapsayan temsil eden nesne. Kapsayan sınıfı yok ise, bir null değer döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu sınıfın temsil, [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) nesnedir, iç içe geçmiş bir sınıf sonra `ppClassField` parametresi döndürür bir `IDebugClassField` sınıfı kapsayan temsil eden nesne. Örneğin, bu sınıf tanımını ele alalım:  
  
```  
class RootClass {  
   class NestedClass { }  
};  
```  
  
 Çağırma `GetEnclosingClass` metodunda `IDebugClassField` nesnesini temsil eden `NestedClass` sınıfı döndürür bir `IDebugClassField` sınıfı temsil eden nesne `RootClass`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)

