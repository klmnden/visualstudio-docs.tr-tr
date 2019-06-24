---
title: Hata ayıklama F# | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Debugging [F#]
- F#, debugging
ms.assetid: 20bcd51c-2d06-4281-9a1e-ef2b91d1a779
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 92f570aece9d68e2a4be20c3487137e085e33001
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62851896"
---
# <a name="debugging-f"></a>Hata ayıklama F\#
Hata ayıklama F# birkaç istisna dışında herhangi bir yönetilen dil hatalarının ayıklanmasına benzer:

- **Otolar** penceresi görüntülemez F# değişkenleri.

- Düzenle ve devam et desteklenmez F#. Düzenleme F# kod hata ayıklama oturumu sırasında mümkündür ancak kaçınılmalıdır. Kod değişiklikleri, hata ayıklama oturumu sırasında uygulanmaz, düzenleme F# hata ayıklama sırasında kodu kaynak kodu ve hata ayıklaması yapılan kod arasında bir uyuşmazlık neden olur.

- Hata ayıklayıcı tanımıyor F# ifadeler. Bir hata ayıklayıcı penceresinde veya bir iletişim kutusu sırasında bir ifade girmenizi F# Çevir gerekir, hata ayıklama ifadesine C# söz dizimi. Çevirme ne zaman bir F# ifadeye C#, unutulmaması emin olun C# kullanır ve eşitlik için karşılaştırma işleci olarak == F# tek = kullanır.

## <a name="see-also"></a>Ayrıca Bkz.
- [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)
