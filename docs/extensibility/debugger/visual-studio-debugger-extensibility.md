---
title: Visual Studio hata ayıklayıcı genişletilebilirliği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Visual Studio], Debugging SDK
- Debugging SDK
ms.assetid: c088b6a2-c3ad-446b-830d-9c6f41b2934b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4184ae40a91e05b1110aed8d3e9b9c9edc64a06d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321472"
---
# <a name="visual-studio-debugger-extensibility"></a>Visual Studio hata ayıklayıcı genişletilebilirliği
Visual Studio, programınızdaki hataları aşağı izlemek için güçlü ve kullanımı kolay bir araç sağlayan bir tam etkileşimli kaynak kodu hata ayıklayıcı, içerir. Hata ayıklayıcı tam destek Visual Basic, C#, C/C++ ve JavaScript sahiptir. Bununla birlikte, [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)], yani kullanılabilir [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=214453), hata ayıklayıcı aynı zengin özelliklere sahip başka bir programlama dili desteklenebilir.

 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Hata ayıklayıcısı, hataları ayıklanan diline özgü buna karşılık olarak hata ayıklama bileşenlerini genel ön uç (diğer bir deyişle, kullanıcı arabirimi) etmektir. İçin gerekli olan tüm yeni diller için destek [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklayıcı, hata ayıklama altyapısı (DE) gibi gerekli arka uç bileşenlerine oluşturmaktır. Bu noktaya yerdir [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] halinde sunulur.

 [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Tüm eksiksiz bir başvuru içeriyor [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] yeni DE oluşturmak için gereken öğeleri. Ayrıca, örnekler ve başlamanıza yardımcı olacak öğreticiler vardır.

 Hata ayıklama desteği ile bir dil proje sisteminin eksiksiz bir örnek için bkz. [IronPython örnek](https://www.microsoft.com/download/details.aspx?id=55984).

 Aşağıdaki bölümlerde kullanarak hata ayıklayıcıyı genişletmek nasıl [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)].

## <a name="in-this-section"></a>Bu bölümde
 [Başlama](../../extensibility/debugger/getting-started-with-debugger-extensibility.md) açıklanmıştır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] teklifler ve SDK'yı yüklemeyi nasıl hata ayıklama.

 [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md) programınızı DE ayırmak için bir DE hazırlama özel DE işlemin, belgeleri.

 [Bir CLR ifade değerlendiricisi yazma](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md) ifade değerlendiricisi yazma olup olmadığını açıklar.

 [Hata ayıklama altyapısı uygulama stratejisi seçme](../../extensibility/debugger/choosing-a-debug-engine-implementation-strategy.md) sizin DE uygulamak nasıl ele alınmaktadır.

 [Başvuru](../../extensibility/debugger/reference/reference-visual-studio-debugging-apis.md) belgeleri [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] hata ayıklama API'si.

 [Örnekleri](../../extensibility/debugger/visual-studio-debugging-samples.md) bir ortak dil çalışma zamanı ifade değerlendiricisi örneği ve bir hata ayıklama altyapısı örneği için bağlantılar içerir.
