---
title: IEEVisualizerDataProvider::SetObjectForVisualizer | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IEEVisualizerDataProvider::SetObjectForVisualizer
helpviewer_keywords:
- IEEVisualizerDataProvider::SetObjectForVisualizer method
ms.assetid: 40dad2be-57ff-4f74-9d82-c48039c125c4
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d20164e31f8c42b7099f99ff34ac120319a2def1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54787623"
---
# <a name="ieevisualizerdataprovidersetobjectforvisualizer"></a>IEEVisualizerDataProvider::SetObjectForVisualizer
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem Görselleştirici temsil eden nesneyi değiştirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetObjectForVisualizer(  
   IDebugObject*  pNewObject,  
   BSTR*          error,  
   IDebugObject** pException  
);  
```  
  
```csharp  
int SetObjectForVisualizer(  
   IDebugObject     pNewObject,  
   out string       error,  
   out IDebugObject pException  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pNewObject`  
 [in] Ayarlanacağı nesne.  
  
 `error`  
 [out] Bu dize, nesne ayarlanırken bir hata oluştu, hata iletisi tutar.  
  
 `pException`  
 [out] Bir hata varsa, bu nesne, özel durum bilgilerini tutar.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu, nasıl hata bilgileri döndürülür belirlemek için en fazla uygulayan olur. Ancak, bir hata olduğunda bu yöntem her zaman bir özel durum nesnesi döndürmelidir bu nedenle bir özel durum nesnesi var. bilmek döndürüldü, görmek için Görünüm, bir hata oluştu. yalnızca bazı çağıranlar olabilir mümkündür. Çağıranın olun ister durumunda hata dizesi ayrıca sağlanan bunu kullanın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
