---
title: Hata ayıklama altyapısı uygulama stratejisi seçme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, implementation strategies
ms.assetid: 90458fdd-2d34-4f10-82dc-6d8f31b66d8b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 930908b66b5d2234b8c62585b10ddf751c96f61c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324503"
---
# <a name="choose-a-debug-engine-implementation-strategy"></a>Hata ayıklama altyapısı uygulama stratejisi seçme
Hata ayıklama altyapısı (DE) uygulaması stratejinizi belirleme için çalışma zamanı mimarisi kullanın. Hata ayıklama altyapısı işlem içi hata ayıklama programına oluşturabilirsiniz. Hata ayıklama altyapısı işlem içinde Visual Studio oturumu hata ayıklama Yöneticisi (SDM) oluşturun. Veya hata ayıklama altyapısı giden işlem her ikisine de oluşturabilirsiniz. Aşağıdaki yönergeler bu üç stratejiler arasında seçmenize yardımcı olmalıdır.

## <a name="guidelines"></a>Kuralları
 İşlem dışı olması için DE mümkün olmakla birlikte SDM ve hata ayıklaması program için genellikle Bunu yapmak için bir neden yoktur. Çağrıları işlem sınırları boyunca görece yavaş yükleniyor.

 Hata ayıklama altyapıları ve ortak dil çalışma zamanı ortamı Win32 yerel çalışma zamanı ortamı için zaten sağlanır. Her iki ortam için DE değiştirmek varsa, işlemdeki DE SDM ile oluşturmanız gerekir.

 Aksi takdirde DE işlem içinde SDM oluşturun veya ayıkladığınız işlemde program. İfade değerlendirici DE, sık kullanılan program simge deposuna erişimi gerektirip gerektirmediğini göz önünde bulundurmanız gerekir. Veya, hızlı erişim için belleğe simge deposundaki yüklü. Ayrıca, aşağıdaki yaklaşımlardan göz önünde bulundurun:

- İfade değerlendirici ve sembol deposundaki arasında birçok çağrı varsa veya sembol deposu SDM bellek alanı okunabiliyorsa DE işlem içinde SDM oluşturun. Programınızı ekler, SDM için hata ayıklama altyapısı CLSID değeri döndürmesi gerekir. SDM bu CLSID DE bir işlem örneğini oluşturmak için kullanır.

- Sembol deposuna erişmek için program DE çağırmanız gerekir, işlemdeki DE programla oluşturun. Bu durumda, program DE örneğini oluşturur.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)