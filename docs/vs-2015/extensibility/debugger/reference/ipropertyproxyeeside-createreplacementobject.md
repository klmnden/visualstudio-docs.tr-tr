---
title: IPropertyProxyEESide::CreateReplacementObject | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IPropertyProxyEESide::CreateReplacementObject
helpviewer_keywords:
- IPropertyProxyEESide::CreateReplacementObject
ms.assetid: 0cfe79b8-c3f1-48b0-a225-e39dee2c92fe
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c3a21e640d6661f8066609bdc344299ccbd63d52
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54800103"
---
# <a name="ipropertyproxyeesidecreatereplacementobject"></a>IPropertyProxyEESide::CreateReplacementObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

İfade değerlendirici (EE) için belirli bir veri nesnesinin bir kopyasını oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CreateReplacementObject(  
   IEEDataStorage*  dataIn,  
   IEEDataStorage** dataOut  
);  
```  
  
```csharp  
int CreateReplacementObject(  
   IEEDataStorage     dataIn,  
   out IEEDataStorage dataOut  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dataIn`  
 [in] Bir [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) kopyalanacak verileri tutan nesne.  
  
 `dataOut`  
 [out] Yeni bir `IEEDataStorage` nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem verilen bir [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) bayt dizisini temsil eden nesne. Bu gelen veri nesnesi tarafından EE genellikle uygulanmadı. Ancak, bu yöntem tarafından döndürülen nesne EE uygulama sağlayan EE tarafından her zaman gerçekleştirilir `IEEDataStorage` ne olursa olsun sınıfı isteniyorsa üzerinde arabirimi.  
  
 Veri gelen tarafından sağlanan Not `IEEDataStorage` nesne giden aynı verileri olmalıdır `IEEDataStorage` nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)
