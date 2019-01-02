---
title: IDebugPortSupplier2::CanAddPort | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPortSupplier2::CanAddPort
helpviewer_keywords:
- IDebugPortSupplier2::CanAddPort
ms.assetid: 41f69e0a-e82c-473d-8b7a-0c40fc5730fc
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 18d728f762a9e4dd16930e4634c9cb0ca47b2bc8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53853911"
---
# <a name="idebugportsupplier2canaddport"></a>IDebugPortSupplier2::CanAddPort
Bağlantı noktası sağlayıcısı yeni bağlantı noktaları ekleyebilirsiniz doğrular.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CanAddPort(   
   void   
);  
```  
  
```csharp  
int CanAddPort();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bağlantı noktası eklenebilir, döndürür `S_OK`; Aksi halde döndürür `S_FALSE` hiçbir bağlantı noktası için bu bağlantı noktası sağlayıcısı eklenebileceğini göstermek için.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemi çağırmadan önce çağrı [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md) ikinci yöntemi bağlantı noktası yanı sıra, zaman alıcı bir işlem olabilir, ekleme oluşturduğundan yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)