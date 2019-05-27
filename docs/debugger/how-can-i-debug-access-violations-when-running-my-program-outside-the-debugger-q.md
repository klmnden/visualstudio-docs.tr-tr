---
title: Uygulama hata ayıklayıcı dışında çalıştırırken erişim İhlallerinde hata ayıklama
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.access
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- access violation debugging
- debugging [Visual Studio], access violations
ms.assetid: 780a298a-132e-4245-8370-8c82ca27c6c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d42dd206117885a23a6c1c15c712be4dc4cd8fe2
ms.sourcegitcommit: 13ab9a5ab039b070b9cd9251d0b83dd216477203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2019
ms.locfileid: "66177670"
---
# <a name="how-can-i-debug-access-violations-when-running-my-program-outside-the-debugger"></a>Kendi Programımı Hata Ayıklayıcı Dışında Çalıştırırken Erişim İhlallerinde Nasıl Hata Ayıklayabilirim?

## <a name="problem-description"></a>Sorun açıklaması
 Kendi programımı Visual Studio ortamında düzgün çalışıyor, ancak bu tek başına Windows işletim sistemiyle birlikte çalıştırabilir, erişim ihlali üretir. Bu sorunu nasıl hata ayıklaması yapabilirsiniz?

## <a name="solution"></a>Çözüm
 Ayarlama [Just-ın-time hata ayıklama](../debugger/just-in-time-debugging-in-visual-studio.md) seçenek ve erişim ihlali gerçekleşene kadar tek başına programınızı çalıştırın. Ardından **erişim ihlali** iletişim kutusu, tıklayabilirsiniz **iptal** hata ayıklayıcıyı başlatmak için.

## <a name="see-also"></a>Ayrıca Bkz.
- [Yerel Kodda Hata Ayıklama SSS](../debugger/debugging-native-code-faqs.md)
- [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)