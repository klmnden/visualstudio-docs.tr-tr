---
title: 'Nasıl yapılır: Yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına Adımlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- SQL
- VB
- CSharp
- C++
helpviewer_keywords:
- Call Stack window, missing native frames
- code, managed code
- native frames
- stepping, out of managed code
- managed code, stepping out of
ms.assetid: 97cdd2a8-02a9-4a06-a5b1-c92b1e431979
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 684738fd2180a3c5bf269b2a30efd970bcf9ab08
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60092207"
---
# <a name="how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window"></a>Nasıl yapılır: Yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına adımla
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kodunuzu görünmez yerel çerçeveler varsa **çağrı yığını** yönetilen kodların dışına Adımlama penceresi, beklenmeyen sonuçlar verebilir. Geçici çözüm olarak, bir kesme noktası yerine kullanabileceğiniz **Step Out**.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-display"></a>Yerel çerçeveler çağrı yığını görüntüden eksik olmadığında yönetilen kodların dışına geçirmek  
  
1. Yerel kodda, yönetilen kod çağrısından sonra bir konum kesme noktası ayarlayın.  
  
2. Üzerinde **hata ayıklama** menüsünde seçin **devam**.  
  
     Yönetilen çağrı yapıldığında yürütme yerel kodda kesme noktasında durur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)
