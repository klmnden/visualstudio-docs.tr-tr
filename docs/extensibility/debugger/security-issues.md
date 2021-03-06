---
title: Güvenlik sorunları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- security [Debugging SDK]
- debugging [Debugging SDK], security
ms.assetid: d6ffff0a-afb4-4f38-86d8-476c881c4e4b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4dc31022611d7148d2cb52182b2a10336215afdc
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345624"
---
# <a name="security-issues"></a>Güvenlik sorunları
Visual Studio kullanarak bir programda hata ayıklamak için gerekli olan tek izinlere olanları programı çalıştırmak için bir geliştirici gerektirir aynıdır. Bu, çoğu durum için uzaktan hata ayıklamayı içerir. Internet bilgi hizmeti gibi diğer hizmetlerle ilgili bazı durumlarda, daha yüksek bir izin düzeyi gerektirebilir.

 Visual Studio çalışırken, işlem hata ayıklama Yöneticisi (PDM) yerel makine üzerinde hata ayıklama işlemlerini izler. Uzaktan adlı bir programı *msvsmon.exe* uzaktan hata ayıklama işlemek ve PDM kullanılabilir hale getirmek için geliştirici tarafından başlatılır. (*msvsmon.exe* hizmet değildir ve bu makinede uzaktan hata ayıklamayı etkinleştirmek için el ile başlatılması gerekir.) Visual Studio (veya *msvsmon.exe*) olan çalışmıyor, hiçbir işlem hata ayıklama için izlenir.

 Bir geliştirici, hiçbir özel izinlerle başladıklarını programlar ayıklayabilirsiniz. Geliştirici, başka bir kişi aynı güvenlik grubunun bir üyesi ise başkası tarafından başlatılan işlemler bile hata ayıklaması yapabilirsiniz. Ve uzaktan hata ayıklamayı etkinleştirmek için yalnızca gerekli dosyalar uzak makineye kopyalayın ve başlatmak gerekli olduğu *msvsmon.exe*. Daha fazla bilgi için [uzaktan hata ayıklama](../../debugger/remote-debugging.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)
- [İşlem Hata Ayıklama Yöneticisi](../../extensibility/debugger/process-debug-manager.md)
- [Uzaktan hata ayıklama](../../debugger/remote-debugging.md)
