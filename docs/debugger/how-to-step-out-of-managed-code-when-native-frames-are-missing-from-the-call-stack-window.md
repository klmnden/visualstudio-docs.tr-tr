---
title: 'Nasıl yapılır: yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına Adımlama | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
helpviewer_keywords:
- Call Stack window, missing native frames
- code, managed code
- native frames
- stepping, out of managed code
- managed code, stepping out of
ms.assetid: 97cdd2a8-02a9-4a06-a5b1-c92b1e431979
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: e5c671f93e20da108a9fd1069a0950f52ef00da9
ms.sourcegitcommit: dd839de3aa24ed7cd69f676293648c6c59c6560a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/27/2018
ms.locfileid: "52388575"
---
# <a name="how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window"></a>Nasıl Yapılır: Yerel Çerçeveler Çağrı Yığını Penceresinde Olmadığında Yönetilen Kodların Dışına Adımlama

Kodunuzu görünmez yerel çerçeveler varsa **çağrı yığını** yönetilen kodların dışına Adımlama penceresi, beklenmeyen sonuçlar verebilir. Geçici çözüm olarak, bir kesme noktası yerine kullanabileceğiniz **Step Out**.

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-display"></a>Yerel çerçeveler çağrı yığını görüntüden eksik olmadığında yönetilen kodların dışına adımla

1.  Yerel kodda, yönetilen kod çağrısından sonra bir konum kesme noktası ayarlayın.

2.  Üzerinde **hata ayıklama** menüsünde seçin **devam**.

     Yönetilen çağrı yapıldığında yürütme yerel kodda kesme noktasında durur.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl Yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)