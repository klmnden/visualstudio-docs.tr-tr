---
title: Yerel kod iş parçacıklarında hata ayıklama ipuçları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], threads
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 8f76a6ea66396a8c5780731945cad87eab94b8ee
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56717604"
---
# <a name="tips-for-debugging-threads-in-native-code"></a>Yerel Kod İş Parçacıklarında Hata Ayıklama İpuçları
Yerel kod iş parçacıklarında hata ayıklama sırasında kullanabileceğiniz bazı ipuçları şunlardır:

-   Yazarak iş parçacığı bilgileri bloğu içeriğini görüntüleyebilirsiniz `@TIB` içinde **Watch** penceresi veya **QuickWatch** iletişim kutusu.

-   Geçerli iş parçacığı için son hata kodunu girerek görüntüleyebileceğiniz `@Err` içinde **Watch** penceresi veya **QuickWatch** iletişim kutusu.

-   C çalışma zamanı kitaplıkları (CRT) işlevleri, çok iş parçacıklı uygulamada hata ayıklama için yararlı olabilir. Daha fazla bilgi için [_malloc_dbg](/cpp/c-runtime-library/reference/malloc-dbg).

## <a name="see-also"></a>Ayrıca Bkz.
- [Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)
- [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)