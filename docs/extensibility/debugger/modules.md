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
ms.openlocfilehash: 1f31e3760a0697be8c9fc80eb811c99df79d32b1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718917"
---
# <a name="modules"></a>Modüller
Hata ayıklayıcı mimarisi bakımından bir *Modülü*:

-   Kod, bir yürütülebilir dosya veya bir DLL gibi fiziksel bir kapsayıcıdır.

-   Onun semboller yeniden yükleyin ve kendisini açıklar. Modül tanımları, IDE'nin modülleri penceresinde görüntülenir.

-   Tarafından temsil edilen bir [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md) arabirimi, modül tanımlamak için hata ayıklama altyapısı tarafından oluşturuldu.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md)