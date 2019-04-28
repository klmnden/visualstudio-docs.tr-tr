---
title: Modüller | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- modules
- debugging [Debugging SDK], modules
ms.assetid: c4cf2809-dbdb-4e75-9273-b3d3d77b67d0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 611d067030cd935f6957a976c8a3aa2b7d4f8ae3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62925409"
---
# <a name="modules"></a>Modüller
Hata ayıklayıcı mimarisi bakımından bir *Modülü*:

- Kod, bir yürütülebilir dosya veya bir DLL gibi fiziksel bir kapsayıcıdır.

- Onun semboller yeniden yükleyin ve kendisini açıklar. Modül tanımları, IDE'nin modülleri penceresinde görüntülenir.

- Tarafından temsil edilen bir [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md) arabirimi, modül tanımlamak için hata ayıklama altyapısı tarafından oluşturuldu.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md)