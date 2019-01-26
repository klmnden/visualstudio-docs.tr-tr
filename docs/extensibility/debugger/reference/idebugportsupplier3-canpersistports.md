---
title: IDebugPortSupplier3::CanPersistPorts | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPortSupplier3::CanPersistPorts
helpviewer_keywords:
- IDebugPortSupplier3::CanPersistPorts
ms.assetid: 4127760c-e602-4e86-9232-457e382a52c7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 78d66f9d267745c1e39c7fc007680009f8881eb4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54933795"
---
# <a name="idebugportsupplier3canpersistports"></a>IDebugPortSupplier3::CanPersistPorts
Bu yöntem, bağlantı noktası sağlayıcısı bağlantı noktası (bunları diske yazarak) hata ayıklayıcı çağrıları arasında kalıcı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CanPersistPorts();  
```  
  
```csharp  
int CanPersistPorts();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 `S_OK` bağlantı noktalarını kalıcı ise veya `S_FALSE` bağlantı noktaları kalıcı belirtmek için.  
  
## <a name="remarks"></a>Açıklamalar  
 Bağlantı noktası sağlayıcısı bağlantı noktası ederse, kaldırıldığında Bunu yapmak ve sonra bunları yeniden başlatıldığında yeniden gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)