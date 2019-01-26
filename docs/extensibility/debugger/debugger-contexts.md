---
title: Hata ayıklayıcı bağlamları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 79808036-b680-4e4c-9c61-4ed43aa11323
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6a9f75167f45b364757326ddb50ef93edfc37104
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55004376"
---
# <a name="debugger-contexts"></a>Hata ayıklayıcı bağlamları
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, hata ayıklama altyapısı (DE) aynı anda birçok farklı bağlamları içinde şu şekilde çalışır:  
  
-   Kod bağlamı bir programın yürütülmesine stream'de geçerli konumu açıklar.  
  
-   Belge bağlamı veya konum, kaynak belge içindeki geçerli konumu açıklar.  
  
-   Hangi ifadesinde değerlendirmesi yer alacak bağlam tanımlayan ifade değerlendirme bağlamı.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Kod bağlamı](../../extensibility/debugger/code-context.md)  
 Bugünün çalışma zamanı mimarileri nontraditional diller ve burada kod yönergeleri, ancak başka bir yolla tarafından temsil edilebilir değil, bir programın yönerge stream'de adresi olarak kod bağlamı anlatır.  
  
 [Belge konumu](../../extensibility/debugger/document-position.md)  
 Visual Studio IDE'ye bilinen kaynak dosyada bir konumdaki bir soyutlama yoluyla hata ayıklama belge konumunu tanımlar.  
  
 [Belge bağlamı](../../extensibility/debugger/document-context.md)  
 Açıklar bir kaynak dosya ile ilgili olarak Visual Studio hata ayıklama hangi belge bağlamı temsil eder. Ayrıca, sembol işleyici kod bağlamı belge bağlamına nasıl eşlendiğini anlatılmaktadır.  
  
 [İfade değerlendirme bağlamı](../../extensibility/debugger/expression-evaluation-context.md)  
 Visual Studio'da bir ifade değerlendirme bağlamı hakkında bilgi sağlar. Örneğin, bir yığın çerçevesiyle ilgili bir ifade değerlendirme bağlamı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri değerlendirmesi için bağlamı sağlar.  
  
## <a name="related-sections"></a>İlgili bölümler  
 [Hata ayıklama kavramları](../../extensibility/debugger/debugger-concepts.md)  
 Hata ayıklama ana mimari kavramlarını açıklar.  
  
 [Hata ayıklama bileşenleri](../../extensibility/debugger/debugger-components.md)  
 Hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) Visual Studio hata ayıklama Bileşenleri'ne genel bakış sağlar.  
  
 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)  
 Program başlatma ve ifadeleri değerlendirme gibi çeşitli hata ayıklama görevlerini bağlantılar içerir.