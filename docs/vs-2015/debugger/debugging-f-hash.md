---
title: Hata ayıklama F# | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- Debugging [F#]
- F#, debugging
ms.assetid: 20bcd51c-2d06-4281-9a1e-ef2b91d1a779
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6e0fd75d45d42fb4216e96c29d1403e89eb44353
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765307"
---
# <a name="debugging-f"></a>F# Hata Ayıklama #
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hata ayıklama F# birkaç istisna dışında herhangi bir yönetilen dil hatalarının ayıklanmasına benzer:  
  
-   **Otolar** penceresi görüntülemez F# değişkenleri.  
  
-   Düzenle ve devam et desteklenmez F#. Düzenleme F# kod hata ayıklama oturumu sırasında mümkündür ancak kaçınılmalıdır. Kod değişiklikleri, hata ayıklama oturumu sırasında uygulanmaz, düzenleme F# hata ayıklama sırasında kodu kaynak kodu ve hata ayıklaması yapılan kod arasında bir uyuşmazlık neden olur.  
  
-   Hata ayıklayıcı tanımıyor F# ifadeler. Bir hata ayıklayıcı penceresinde veya bir iletişim kutusu sırasında bir ifade girmenizi F# Çevir gerekir, hata ayıklama ifadesine C# söz dizimi. Çevirme ne zaman bir F# ifadeye C#, unutulmaması emin olun C# kullanır ve eşitlik için karşılaştırma işleci olarak == F# tek = kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)
