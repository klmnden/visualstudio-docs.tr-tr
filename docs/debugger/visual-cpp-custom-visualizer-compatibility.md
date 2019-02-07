---
title: Visual C/C++ özel Görselleştirici uyumluluğu
ms.date: 01/28/2019
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- debugging assertions
- assertions, debugging
- assertions, assertion failures
- Assertion Failed dialog box
ms.assetid: 64af5bed-e38b-420f-b9ce-d64f35100aae
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
monikerRange: '>= vs-2019'
ms.openlocfilehash: 3c90c66e338330d77af29564c7586e68b8ee35b6
ms.sourcegitcommit: 01334abf36d7e0774329050d34b3a819979c95a2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55852614"
---
# <a name="visual-cc-custom-visualizer-compatibility"></a>Visual C/C++ özel Görselleştirici uyumluluğu

Visual Studio 2019 ' başlayarak, Visual C++ bellek kullanımı yoğun bileşenlerinden barındırmak için bir dış 64-bit işlem kullanan gelişmiş bir hata ayıklayıcı içerir. Bu güncelleştirmenin bir parçası, bazı uzantılar Visual C/C++ ifade değerlendiricisi yeni hata ayıklayıcısı ile uyumlu olacak şekilde güncelleştirilmesi gerekir.

Şu anda eski C/C++ EE eklentisi veya C/C++ özel Görselleştirici kullanma seçerseniz, bu dış işlem kullanımını devre dışı giderek kapatabilirsiniz **Araçları** > **seçenekleri**  >   **Hata ayıklama**ve ardından seçimini **yük hata ayıklama sembolleri dış işlemde (yalnızca yerel)**. Bu seçeneğin işaretini kaldırın IDE (devenv.exe) işlem içindeki bellek kullanımında önemli bir artış meydana gelir. Büyük projeler hata ayıklamak bekliyorsanız, bu nedenle, bu hata ayıklama seçeneği ile uyumlu hale getirmek için uzantı sahibi çalışmak önerilir.

Eski C/C++ EE eklentisi veya C/C++ özel Görselleştirici sahibiyseniz, bir çalışan işlemindeki uzantınız yükleniyor içine seçim yapma hakkında daha fazla bilgi bulabilirsiniz [Concord genişletilebilirlik örnekleri wiki](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Worker-Process-Remoting). Ayrıca bulabilirsiniz bir [C/C++ özel Görselleştirici örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/tree/master/CppCustomVisualizer).