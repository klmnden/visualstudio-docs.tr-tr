---
title: Modüller | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- modules
- debugging [Debugging SDK], modules
ms.assetid: c4cf2809-dbdb-4e75-9273-b3d3d77b67d0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b231ee1eb84f41115a0892cda42a8b7e781e5e53
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350673"
---
# <a name="modules"></a>Modüller
Hata ayıklayıcı mimarisi bakımından bir *Modülü*:

- Kod, bir yürütülebilir dosya veya bir DLL gibi fiziksel bir kapsayıcıdır.

- Onun semboller yeniden yükleyin ve kendisini açıklar. Modül tanımları, IDE'nin modülleri penceresinde görüntülenir.

- Tarafından temsil edilen bir [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md) arabirimi, modül tanımlamak için hata ayıklama altyapısı tarafından oluşturuldu.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md)