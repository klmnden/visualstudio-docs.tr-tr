---
title: Visual C/C++ özel Görselleştirici uyumluluğu
ms.date: 01/28/2019
ms.prod: visual-studio-dev16
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- debugging assertions
- assertions, debugging
- assertions, assertion failures
- Assertion Failed dialog box
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
monikerRange: '>= vs-2019'
ms.openlocfilehash: 32e38dd3bba8a1127d8756972b73e8b47a514f1b
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2019
ms.locfileid: "56335187"
---
# <a name="visual-cc-custom-visualizer-compatibility"></a>Visual C/C++ özel Görselleştirici uyumluluğu

Visual Studio 2019 ' başlayarak, Visual C++ bellek kullanımı yoğun bileşenlerinden barındırmak için bir dış 64-bit işlem kullanan gelişmiş bir hata ayıklayıcı içerir. Bu güncelleştirmenin bir parçası, bazı uzantılar Visual C/C++ ifade değerlendiricisi yeni hata ayıklayıcısı ile uyumlu olacak şekilde güncelleştirilmesi gerekir.

Şu anda eski C/C++ EE eklentisi veya C/C++ özel Görselleştirici kullanma seçerseniz, bu dış işlem kullanımını devre dışı giderek kapatabilirsiniz **Araçları** > **seçenekleri**  >   **Hata ayıklama**ve ardından seçimini **yük hata ayıklama sembolleri dış işlemde (yalnızca yerel)**. Bu seçeneğin işaretini kaldırın IDE (devenv.exe) işlem içindeki bellek kullanımında önemli bir artış meydana gelir. Büyük projeler hata ayıklamak bekliyorsanız, bu nedenle, bu hata ayıklama seçeneği ile uyumlu hale getirmek için uzantı sahibi çalışmak önerilir.

Eski C/C++ EE eklentisi veya C/C++ özel Görselleştirici sahibiyseniz, bir çalışan işlemindeki uzantınız yükleniyor içine seçim yapma hakkında daha fazla bilgi bulabilirsiniz [Concord genişletilebilirlik örnekleri wiki](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Worker-Process-Remoting). Ayrıca bulabilirsiniz bir [C/C++ özel Görselleştirici örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/tree/master/CppCustomVisualizer).