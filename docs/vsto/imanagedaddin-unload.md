---
title: IManagedAddin::Unload
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Unload method
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 296502aa461688c34152d86ee21aab5f2c83ecb4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62956750"
---
# <a name="imanagedaddinunload"></a>IManagedAddin::Unload
  Hemen önce çağrılır yönetilen bir VSTO eklentisi kaldırılır.

## <a name="syntax"></a>Sözdizimi

```csharp
HRESULT Unload();
```

## <a name="return-value"></a>Dönüş değeri
 Yöntemi başarıyla tamamlanıp tamamlanmadığını belirten bir HRESULT değer.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, geçerli Microsoft Office sürümleri tarafından çağrılmaz. Bu yöntem, gelecekte kullanılmak üzere ayrılmıştır.

## <a name="see-also"></a>Ayrıca bkz.
- [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md)
- [IManagedAddin::Load](../vsto/imanagedaddin-load.md)
