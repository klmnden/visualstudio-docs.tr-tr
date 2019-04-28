---
title: Paket hatalarını ayıklama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], packages
ms.assetid: 99947fd4-fb87-4c69-b26c-65634e17d285
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2ba784f3a544b2f66f1f2c9c229f85477bf6c782
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62890045"
---
# <a name="debug-package"></a>Paket hatalarını ayıklama
Hata ayıklama paketi, Visual Studio Kabuğu'nda çalışır ve tüm UI işler. Visual Studio hata ayıklama arabirimleri kullanır ve oturum hata ayıklama Yöneticisi (SDM) ile iletişim kurar.

 SDM gönderilen break olayları kesme modu ve odağı sonu oluştuğu programın değiştirmek için hata ayıklayıcı çalışma modundan geçin. Hata ayıklama paketi olaylar tarafından gönderilen bilgileri yığın çerçevesi ve iş parçacığı izler.

 Hata ayıklama paketi hiçbir dil veya çalışma zamanı ortamı bağımlılıkları vardır. Uygulama veya hata ayıklama paketi değiştirmek gerekli değildir.

 Hata ayıklama paketi tarafından uygulanan *vsdebug.dll*.

## <a name="see-also"></a>Ayrıca bkz.
- [Oturum hata ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)
- [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)
- [İş Parçacıkları](../../extensibility/debugger/threads.md)
- [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)