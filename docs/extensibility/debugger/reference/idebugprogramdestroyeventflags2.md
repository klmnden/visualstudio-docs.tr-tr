---
title: IDebugProgramDestroyEventFlags2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c1b131679a287fb555fcf2a78a803c77457d47ca
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66343508"
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