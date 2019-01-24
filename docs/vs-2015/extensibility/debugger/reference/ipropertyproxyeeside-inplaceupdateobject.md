---
title: IPropertyProxyEESide::InPlaceUpdateObject | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IPropertyProxyEESide::InPlaceUpdateObject
helpviewer_keywords:
- IPropertyProxyEESide::InPlaceUpdateObject
ms.assetid: abf89411-1853-4f23-b244-d5e0afa197b1
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c91497815dd18dc138b2eadc462c43785830a033
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54797685"
---
# <a name="ipropertyproxyeesideinplaceupdateobject"></a>IPropertyProxyEESide::InPlaceUpdateObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Nesnenin veri belirli bir veri nesnesini güncelleştirir ve yeni nesnenin veri temsil eden yeni bir veri nesnesini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT InPlaceUpdateObject(  
   [in] IEEDataStorage*   dataIn,  
   [out] IEEDataStorage** dataOut  
);  
```  
  
```csharp  
int InPlaceUpdateObject(  
   IEEDataStorage     dataIn,  
   out IEEDataStorage dataOut  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dataIn`  
 [in] Bir [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) yeni veri içeren nesne.  
  
 `dataOut`  
 [out] Yeni bir `IEEDataStorage` değiştirilen verileri içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, nesnenin veri gerçekten güncelleştirir. Döndürülen verileri [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) nesne gelen verileri aynı olması gerekmez `IEEDataStorage` döndürülen nesnesi özelliğin geçerli değerini yansıtmak gerekir.  
  
 Gelen veri nesnesi tarafından EE genellikle uygulanmadı. Ancak, bu yöntem tarafından döndürülen nesne EE uygulama sağlayan EE tarafından her zaman gerçekleştirilir `IEEDataStorage` ne olursa olsun sınıfı isteniyorsa üzerinde arabirimi.  
  
 [CreateReplacementObject](../../../extensibility/debugger/reference/ipropertyproxyeeside-createreplacementobject.md) yöntem gelen veri nesnesini temel alan bir veri nesnesi oluşturur, ancak özelliğin özgün verileri etkilemez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [CreateReplacementObject](../../../extensibility/debugger/reference/ipropertyproxyeeside-createreplacementobject.md)
