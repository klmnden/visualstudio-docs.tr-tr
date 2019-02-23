---
title: IDebugPortSupplier3::CanPersistPorts | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
ms.openlocfilehash: ad31d015048d8e0732c32652141b7be060628663
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56722635"
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
- [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)