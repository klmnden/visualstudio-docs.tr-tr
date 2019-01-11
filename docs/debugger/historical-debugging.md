---
title: Geçmiş hata ayıklama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 7cc5ddf2-2f7c-4f83-b7ca-58e92e9bfdd2
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: dc16c6e6186d53bd08bd0634e07a4d1172859280
ms.sourcegitcommit: 01185dadd2fa1f9a040d2a366869f1a5e1d18e0f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54227258"
---
# <a name="historical-debugging-c-visual-basic-c"></a>Geçmiş hata ayıklama (C#, Visual Basic, C++)

Geçmiş hata ayıklama IntelliTrace tarafından toplanan bilgiler bağımlı hata ayıklama bir moddur. Geriye doğru gitme ve uygulamanızın yürütmesini iletmek ve durumunu incelemek sağlar.  
  
 IntelliTrace, Visual Studio Enterprise edition (ancak Professional veya Community sürümlerini değil) kullanabilirsiniz.  
  
## <a name="why-use-historical-debugging"></a>Geçmiş hata ayıklama neden kullanmalısınız?

 Hataları bulmak için kesme noktaları ayarlamak yerine hit-or-miss affair olabilir. Kodunuzda yakın bir yerde olması için hata nerede şüphelendiğiniz bir kesme noktası ayarlayın ve ardından hata ayıklayıcı ve kesme noktasına isabet ve burada yürütmeyi keser yerde hatanın kaynağını ortaya koyabilir alır soluk uygulamayı çalıştırın. Aksi durumda, kod içinde başka bir yerde bir kesme noktası ayarlamayı deneyin ve sorun bulana kadar test adımlarınızı tekrar tekrar yürütme hata ayıklayıcıyı yeniden çalıştırmak sahip olacaksınız.  
  
 ![bir kesme noktası ayarlamak](../debugger/media/breakpointprocesa.png "BreakpointProcesa")  
  
 Geçici uygulamanızdaki dolaşan ve kesme noktaları ayarlayın, hata ayıklamayı yeniden başlatmak zorunda kalmadan (çağrı yığını ve yerel değişkenler) durumunu incelemek için IntelliTrace ve geçmiş hata ayıklama kullanın ve test adımları yineleyin. Bu, çok fazla kaydedebilirsiniz süresini, özellikle zaman hata bulunan yürütmek için uzun zaman alan derin bir testi senaryosunda.  
  
## <a name="how-do-i-start-using-historical-debugging"></a>Geçmiş hata ayıklama kullanmaya nasıl başlarım?

 IntelliTrace varsayılan olarak açıktır. Yapmanız gereken şey, tam uygulama durumunun anlık görüntülerini görüntülemek istediğiniz ve hangi olayların ve işlev çağrılarının ilginizi çeken karar verin. Aramak istediğiniz tanımlama hakkında daha fazla bilgi için bkz. [IntelliTrace özellikleri](../debugger/intellitrace-features.md). Özellik desteği, dil ve uygulama tarafından değişir türü.

 - Geçmiş hata ayıklama anlık görüntülerini görüntülemek için bkz: [IntelliTrace kullanarak önceki uygulama durumlarını İnceleme](../debugger/view-historical-application-state.md)
 - Değişkenleri incelemek ve koda gitmek öğrenmek için bkz: [geçmiş hata ayıklama ile uygulamanızı denetleyin](../debugger/historical-debugging-inspect-app.md)
 - IntelliTrace olayları ile hata ayıklama hakkında daha fazla bilgi için bkz: [izlenecek yol: IntelliTrace kullanarak](../debugger/walkthrough-using-intellitrace.md).