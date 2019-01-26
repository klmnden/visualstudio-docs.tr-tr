---
title: / Adım C# kodu yerel çerçeveler çağrı yığınından eksik olduğunda | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
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
manager: jillfra
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 25021f0c3daffdaf59633fdb9bff0e2659f43d2e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55043031"
---
# <a name="how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window"></a>Nasıl yapılır: Yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına adımla

Kodunuzu görünmez yerel çerçeveler varsa **çağrı yığını** yönetilen kodların dışına Adımlama penceresi, beklenmeyen sonuçlar verebilir. Geçici çözüm olarak, bir kesme noktası yerine kullanabileceğiniz **Step Out**.

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-display"></a>Yerel çerçeveler çağrı yığını görüntüden eksik olmadığında yönetilen kodların dışına adımla

1.  Yerel kodda, yönetilen kod çağrısından sonra bir konum kesme noktası ayarlayın.

2.  Üzerinde **hata ayıklama** menüsünde seçin **devam**.

     Yönetilen çağrı yapıldığında yürütme yerel kodda kesme noktasında durur.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)