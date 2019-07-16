---
title: Hata ayıklayıcı bağlamları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 79808036-b680-4e4c-9c61-4ed43aa11323
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 771a3cd8ae25173f3033b3a3229e516570f5dedc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200641"
---
# <a name="debugger-contexts"></a>Hata Ayıklayıcı Bağlamları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] hata ayıklama, hata ayıklama altyapısı (DE) aynı anda birçok farklı bağlamları içinde şu şekilde çalışır:  
  
- Kod bağlamı bir programın yürütülmesine stream'de geçerli konumu açıklar.  
  
- Belge bağlamı veya konum, kaynak belge içindeki geçerli konumu açıklar.  
  
- Hangi ifadesinde değerlendirmesi yer alacak bağlam tanımlayan ifade değerlendirme bağlamı.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Kod Bağlamı](../../extensibility/debugger/code-context.md)  
 Bugünün çalışma zamanı mimarileri nontraditional diller ve burada kod yönergeleri, ancak başka bir yolla tarafından temsil edilebilir değil, bir programın yönerge stream'de adresi olarak kod bağlamı anlatır.  
  
 [Belge Konumu](../../extensibility/debugger/document-position.md)  
 Visual Studio IDE'ye bilinen kaynak dosyada bir konumdaki bir soyutlama yoluyla hata ayıklama belge konumunu tanımlar.  
  
 [Belge Bağlamı](../../extensibility/debugger/document-context.md)  
 Açıklar bir kaynak dosya ile ilgili olarak Visual Studio hata ayıklama hangi belge bağlamı temsil eder. Ayrıca, sembol işleyici kod bağlamı belge bağlamına nasıl eşlendiğini anlatılmaktadır.  
  
 [İfade Değerlendirme Bağlamı](../../extensibility/debugger/expression-evaluation-context.md)  
 Visual Studio'da bir ifade değerlendirme bağlamı hakkında bilgi sağlar. Örneğin, bir yığın çerçevesiyle ilgili bir ifade değerlendirme bağlamı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri değerlendirmesi için bağlamı sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Hata ayıklama kavramları](../../extensibility/debugger/debugger-concepts.md)  
 Hata ayıklama ana mimari kavramlarını açıklar.  
  
 [Hata ayıklama bileşenleri](../../extensibility/debugger/debugger-components.md)  
 Hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) Visual Studio hata ayıklama Bileşenleri'ne genel bakış sağlar.  
  
 [Hata Ayıklama Görevleri](../../extensibility/debugger/debugging-tasks.md)  
 Program başlatma ve ifadeleri değerlendirme gibi çeşitli hata ayıklama görevlerini bağlantılar içerir.
