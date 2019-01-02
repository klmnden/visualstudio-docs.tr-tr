---
title: IManagedAddin::Unload
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Unload method
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 4aa3c07ed715a6118bd053d44503607a889f3da7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53880906"
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
 [Imanagedaddin arabirimi](../vsto/imanagedaddin-interface.md)   
 [IManagedAddin::Load](../vsto/imanagedaddin-load.md)  
