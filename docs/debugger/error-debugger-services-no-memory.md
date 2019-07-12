---
title: Hata ayıklayıcı, bellek yetersiz çalışan hizmetler | Microsoft Docs
ms.date: 07/10/2019
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.debug_no_memory
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger
author: isadorasophia
ms.author: isgarcia
manager: caslan
ms.workload:
- multiple
ms.openlocfilehash: 05664ffd056f69215e6fb00d6d49a59382a3692f
ms.sourcegitcommit: da4079f5b6ec884baf3108cbd0519d20cb64c70b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67861173"
---
# <a name="debugger-services-running-out-of-memory"></a>Hata ayıklayıcı, bellek yetersiz çalışan hizmetleri
Hata Ayıklama Hizmetleri bellek yetersiz ve hata ayıklama oturumu sonlandırma neden oldu.

## <a name="to-investigate-this-error-on-windows"></a>Windows üzerinde bu hatayı incelemek için
- İşlem bellek grafikte denetleyebilirsiniz **tanılama araçları** hedef uygulamanın bellek büyük büyüme karşılaşıp penceresini. Bu durumda, kullanın **bellek kullanımı** aracının ne tanılamak için altta yatan sorunu için bkz. [bellek kullanımını analiz etme](../profiling/memory-usage.md).

- Hedef uygulama, çok miktarda bellek kullanan görünmüyor kullanırsanız **Görev Yöneticisi'ni** penceresi için bellek kullanımını Visual Studio (devenv.exe) çalışan işleminden (msvsmon.exe) veya VS Code (vsdbg.exe/vsdbg-ui.exe) denetlemek için hata ayıklayıcı ile ilgili bir sorun olup olmadığını belirler. Bellek yetersiz çalışan işlemi devenv.exe ise, Visual Studio uzantıları çalışan sayısını azaltmayı göz önünde bulundurun.

## <a name="see-also"></a>Ayrıca Bkz.
- [Blog postası: Hata ayıklama sırasında CPU ve bellek çözümleme](https://devblogs.microsoft.com/visualstudio/analyze-cpu-memory-while-debugging/)
- [Bellek yönetimi hakkında](/windows/win32/memory/about-memory-management)
