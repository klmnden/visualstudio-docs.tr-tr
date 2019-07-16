---
title: IDebugClassField::GetEnclosingClass | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugClassField::GetEnclosingClass
helpviewer_keywords:
- IDebugClassField::GetEnclosingClass method
ms.assetid: a0c12e3c-9ea0-4dfb-9e45-8cea18725022
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 896d3ecd5202bf85e6b9e86af31796c662a6eef1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68190998"
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
