---
title: IPropertyProxyProvider::GetPropertyProxy | Microsoft Docs
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
- IPropertyProxyProvider::GetPropertyProxy
helpviewer_keywords:
- IPropertyProxyProvider::GetPropertyProxy
ms.assetid: 3ebb7515-5bfe-48f4-9b8d-721b8f664eb6
caps.latest.revision: 15
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f93c6d34e1b1a2998a72bfa9bf4d950f135de176
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49815802"
---
# <a name="ipropertyproxyprovidergetpropertyproxy"></a>IPropertyProxyProvider::GetPropertyProxy
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Özelliği proxy arabirimi için belirtilen ara sunucu kimliğini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetPropertyProxy(  
   DWORD                  dwID,  
   IPropertyProxyEESide** proxy  
);  
```  
  
```csharp  
int GetPropertyProxy(  
   uint                     dwID,  
   out IPropertyProxyEESide proxy  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwID`  
 [in] İstenen özellik proxy kimliği.  
  
 `proxy`  
 [out] Döndürür bir [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md) nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Dış tür görselleştiricileri desteklemek için bu yöntem genellikle çağrısı iletir [GetPropertyProxy](../../../extensibility/debugger/reference/ieevisualizerservice-getpropertyproxy.md) yöntemi. Bkz: [Visualizing ve verileri görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md) ayrıntılı IEEVisualizerService nasıl elde edilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IPropertyProxyProvider](../../../extensibility/debugger/reference/ipropertyproxyprovider.md)   
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [GetPropertyProxy](../../../extensibility/debugger/reference/ieevisualizerservice-getpropertyproxy.md)   
 [Verileri Görselleştirme ve Görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md)

