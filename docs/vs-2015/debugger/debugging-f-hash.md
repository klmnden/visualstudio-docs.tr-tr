---
title: 'F # hata ayıklama | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
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
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dd722e40a0579181e3c361706f0775aaf350c341
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49209579"
---
# <a name="debugging-f"></a>F# Hata Ayıklama #
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

F # hata ayıklama birkaç istisna dışında herhangi bir yönetilen dil hatalarının ayıklanmasına benzer:  
  
-   **Otolar** pencere, F # değişkenleri görüntülemez.  
  
-   Düzenle ve devam et desteklenmez F # için. F # kodunda hata ayıklama oturumu sırasında düzenleme mümkündür, ancak kaçınılmalıdır. Hata ayıklama sırasında F # kod düzenleme, hata ayıklama oturumu sırasında kod değişikliklerini uygulanmamış olduğundan, kaynak kodu ve hata ayıklaması yapılan kod arasında bir uyuşmazlık neden olur.  
  
-   Hata ayıklayıcı, F # ifadelerini algılamaz. F # hata ayıklama sırasında bir hata ayıklayıcı penceresi ya da iletişim kutusunda bir ifade girmek için C# sözdizimi ifadesine Çevir gerekir. Bir F # ifadesi C# içinde Çevir, C# kullandığını hatırlamak emin olmak için eşitlik ve bu F # karşılaştırma işleci kullandığından tek = ==.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)



