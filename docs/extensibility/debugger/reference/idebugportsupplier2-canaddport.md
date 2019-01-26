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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 650b65e043ca16a5aa73a298025819f2fe6802f6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54942392"
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