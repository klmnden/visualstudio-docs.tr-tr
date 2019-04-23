---
title: Hata ayıklayıcı kaynak kodu veya Ayrıştırılmış kod görüntüleyemiyor | Microsoft Docs
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
- disassembly code, errors
ms.assetid: 112d3ea3-fdd2-4bce-92b4-167a76258934
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5ce4460aecb634523de02f2e3f6929b206b415e3
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60092609"
---
# <a name="debugger-cannot-display-source-code-or-disassembly"></a>Hata Ayıklayıcı Kaynak Kodu veya Ayrıştırılmış Kodu Görüntüleyemez
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu hata görünür:  
  
 Hata ayıklayıcı kaynak kodu veya Ayrıştırılmış kod burada yürütme durduruldu şu anki konum için görüntülenemiyor.  
  
 Bu hata iletisi, bir dizi nedenden ötürü ortaya çıkabilir:  
  
- Bir konum için kaynak kodu yok, ayrıştırılmış kodu desteklemiyor bir dil hata ayıklarken bir kesme noktasına ulaşırsınız. Açık **kesme noktaları** penceresinde kesme noktasını bulun ve silin.  
  
- Betik hata ayıklaması yapıyorsanız programınızdaki iş parçacığı kopyalanırken bir kesme noktası isabet. Seçin **adım** veya **devam** gelen **hata ayıklama** hata ayıklama devam etmek için menü.  
  
- Güvenlik konuları yığın, iş parçacığı, kaydı ve diğer bağlam bilgileriyle hata ayıklaması yaptığınız programı okunurken hata ayıklayıcı engellemiş olabilir. Bir Web uygulaması hata ayıklaması yapıyorsanız ve doğru sanal dizine erişim izni yoksa durum büyük olasılıkla budur. Sanal dizin için güvenlik anonim olarak ayarlayın ve yeniden deneyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcı temel bilgileri](../debugger/debugger-basics.md)   
 [Visual Studio'da hata ayıklama](../debugger/debugging-in-visual-studio.md)   
 [Hata Ayıklayıcıda Verileri Görüntüleme](../debugger/viewing-data-in-the-debugger.md)
