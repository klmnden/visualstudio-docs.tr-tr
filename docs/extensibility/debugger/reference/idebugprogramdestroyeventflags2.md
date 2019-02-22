---
title: IDebugProgramDestroyEventFlags2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: aed4d652a300ac9b18d45456c56a0b9b56285206
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707789"
---
# <a name="idebugprogramdestroyeventflags2"></a>IDebugProgramDestroyEventFlags2
Varsayılan davranışı geçersiz kılmak bir hata ayıklama altyapısı sağlayan [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] hata ayıklama oturumunu sonlandırdığınızda, kullanıcı Arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgramDestroyEventFlags2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim, hata ayıklama motoru tarafından uygulanır. Oluşturma ve bir işlem yaşam süresi boyunca birden çok program yok konaklar için kullanışlıdır.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramDestroyEventFlags2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)|Program alır bayrakları yok.|

## <a name="remarks"></a>Açıklamalar
 Varsayılan davranışını [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] UI olan tüm programları bir program gönderdikten sonra Tasarım moduna geri dönmek için olay yok. Bu arabirim, bu davranışı değiştirmek bir hata ayıklama altyapısı sağlar.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll