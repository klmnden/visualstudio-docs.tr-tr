---
title: IDebugPortSupplier2::CanAddPort | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2::CanAddPort
helpviewer_keywords:
- IDebugPortSupplier2::CanAddPort
ms.assetid: 41f69e0a-e82c-473d-8b7a-0c40fc5730fc
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e4ec078650446d3511ed9c5bdc8ee3ec0191487d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68188353"
---
# <a name="idebugportsupplier2canaddport"></a>IDebugPortSupplier2::CanAddPort
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bağlantı noktası sağlayıcısı yeni bağlantı noktaları ekleyebilirsiniz doğrular.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
