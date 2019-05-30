---
title: Hata ayıklayıcı bağlamları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 79808036-b680-4e4c-9c61-4ed43aa11323
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 011999929fd4cb1508bf4958629e622684f35739
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345991"
---
# <a name="debugger-contexts"></a>Hata ayıklayıcı bağlamları
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama, hata ayıklama altyapısı (DE) aynı anda birçok farklı bağlamları içinde şu şekilde çalışır:

- Kod bağlamı bir programın yürütülmesine stream'de geçerli konumu açıklar.

- Belge bağlamı veya konum, kaynak belge içindeki geçerli konumu açıklar.

- Hangi ifadesinde değerlendirmesi yer alacak bağlam tanımlayan ifade değerlendirme bağlamı.

## <a name="in-this-section"></a>Bu bölümde
 [Kod bağlamı](../../extensibility/debugger/code-context.md) adresi olarak nerede kod değil temsil edilemiyor yönergeleri ancak başka bir yolla bugünün çalışma zamanı mimarileri nontraditional dilleri karşı bir programın yönerge stream'de Discusses kod bağlamı.

 [Belge konumu](../../extensibility/debugger/document-position.md) IDE'ye bilinen bir konumdaki kaynak dosyada bir soyutlama yoluyla Visual Studio hata belge konumunu tanımlar.

 [Belge bağlamı](../../extensibility/debugger/document-context.md) Discusses hangi belge bağlamı, Visual Studio ile ilgili bir kaynak dosyası hata ayıklama temsil eder. Ayrıca, sembol işleyici kod bağlamı belge bağlamına nasıl eşlendiğini anlatılmaktadır.

 [İfade değerlendirme bağlamının](../../extensibility/debugger/expression-evaluation-context.md) Visual Studio'da bir ifade değerlendirme bağlamı hakkında bilgi sağlar. Örneğin, bir yığın çerçevesiyle ilgili bir ifade değerlendirme bağlamı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri değerlendirmesi için bağlamı sağlar.

## <a name="related-sections"></a>İlgili bölümler
 [Hata ayıklama kavramları](../../extensibility/debugger/debugger-concepts.md) ana hata ayıklama mimari kavramlarını açıklar.

 [Hata ayıklama bileşenleri](../../extensibility/debugger/debugger-components.md) Visual Studio hata ayıklama altyapısı (DE) ifade değerlendiricisi (EE) ve sembol işleyici (SH) bileşenleri, hata ayıklama genel bir bakış sağlar.

 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md) çeşitli program başlatma ve ifadeleri değerlendirme gibi hata ayıklama görevleri bağlantılar içerir.