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
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640499"
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
