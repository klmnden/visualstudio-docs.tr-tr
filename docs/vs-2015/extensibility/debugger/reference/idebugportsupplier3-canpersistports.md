---
title: IDebugPortSupplier3::CanPersistPorts | Microsoft Docs
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
- IDebugPortSupplier3::CanPersistPorts
helpviewer_keywords:
- IDebugPortSupplier3::CanPersistPorts
ms.assetid: 4127760c-e602-4e86-9232-457e382a52c7
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: dbaa1a02d780acce0b3c818f9f90103cfed0e683
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49183774"
---
# <a name="idebugportsupplier3canpersistports"></a>IDebugPortSupplier3::CanPersistPorts
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, bağlantı noktası sağlayıcısı bağlantı noktası (bunları diske yazarak) hata ayıklayıcı çağrıları arasında kalıcı olup olmadığını belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CanPersistPorts();  
```  
  
```csharp  
int CanPersistPorts();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 `S_OK` bağlantı noktalarını kalıcı ise veya `S_FALSE` bağlantı noktaları kalıcı belirtmek için.  
  
## <a name="remarks"></a>Açıklamalar  
 Bağlantı noktası sağlayıcısı bağlantı noktası ederse, kaldırıldığında Bunu yapmak ve sonra bunları yeniden başlatıldığında yeniden gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)

