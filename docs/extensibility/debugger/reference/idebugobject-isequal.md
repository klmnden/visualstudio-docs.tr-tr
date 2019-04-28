---
title: IDebugObject::IsEqual | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugObject::IsEqual
helpviewer_keywords:
- IDebugObject::IsEqual method
ms.assetid: 4b76e663-ef2e-41ff-9be1-bf26d666a34a
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 49d909dc0896bcc1b130ce908699c04ad9543c73
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62918511"
---
# <a name="idebugobjectisequal"></a>IDebugObject::IsEqual
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu nesne bir nesneyle karşılaştırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT IsEqual(   
   IDebugObject* pObject,  
   BOOL*         pfIsEqual  
);  
```  
  
```csharp  
int IsEqual(  
   IDebugObject pObject,  
   out int      pfIsEqual  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pObject`  
 [in] Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) karşılaştırma yapılacak nesne temsil eden nesne.  
  
 `pfIsEqual`  
 [out] Sıfır olmayan döndürür (`TRUE`) nesnelerin değerler, eşit; Aksi takdirde, sıfır döndürür (`FALSE`).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Genellikle, bu yöntem tarafından temsil edilen değerleri adresleri karşılaştırabilirsiniz `pObject` parametresi ve bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne; adresleri eşitse sonra nesneler eşit kabul edilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
