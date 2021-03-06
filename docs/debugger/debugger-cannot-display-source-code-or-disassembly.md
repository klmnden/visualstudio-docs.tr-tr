---
title: Hata ayıklayıcı kaynak kodu veya ayrıştırılmış kodu görüntüleyemez
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- disassembly code, errors
ms.assetid: 112d3ea3-fdd2-4bce-92b4-167a76258934
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6ee3181bedc520f24840f1b16221ea21055bf698
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71211170"
---
# <a name="debugger-cannot-display-source-code-or-disassembly"></a>Hata Ayıklayıcı Kaynak Kodu veya Ayrıştırılmış Kodu Görüntüleyemez
Bu hata görünür:

 Hata ayıklayıcı kaynak kodu veya Ayrıştırılmış kod burada yürütme durduruldu şu anki konum için görüntülenemiyor.

 Bu hata iletisi, bir dizi nedenden ötürü ortaya çıkabilir:

- Bir konum için kaynak kodu yok, ayrıştırılmış kodu desteklemiyor bir dil hata ayıklarken bir kesme noktasına ulaşırsınız. Açık **kesme noktaları** penceresinde kesme noktasını bulun ve silin.

- Betik hata ayıklaması yapıyorsanız programınızdaki iş parçacığı kopyalanırken bir kesme noktası isabet. Seçin **adım** veya **devam** gelen **hata ayıklama** hata ayıklama devam etmek için menü.

- Güvenlik konuları yığın, iş parçacığı, kaydı ve diğer bağlam bilgileriyle hata ayıklaması yaptığınız programı okunurken hata ayıklayıcı engellemiş olabilir. Bir Web uygulaması hata ayıklaması yapıyorsanız ve doğru sanal dizine erişim izni yoksa durum büyük olasılıkla budur. Sanal dizin için güvenlik anonim olarak ayarlayın ve yeniden deneyin.

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio’da hata ayıklama](../debugger/index.yml)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [Hata Ayıklayıcıda Verileri Görüntüleme](../debugger/viewing-data-in-the-debugger.md)