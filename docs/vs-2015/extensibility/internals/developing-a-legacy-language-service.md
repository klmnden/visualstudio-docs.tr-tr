---
title: Eski dil hizmeti geliştirme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- vs.vsip.LangServWiz.langtoks
- vs.vsip.LangServWiz.welcome
- vs.vsip.LangServWiz.langSpec
- vs.vsip.LangServWiz.langInfo
- vs.vsip.LangServWiz.langServOpts
helpviewer_keywords:
- language services, developing
ms.assetid: 6151ba88-c1c3-41de-a1cc-668f494d48d1
caps.latest.revision: 29
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0a4477249dfad57bb75a83b40d6c3b1a4343a23f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54798571"
---
# <a name="developing-a-legacy-language-service"></a>Eski Dil Hizmeti Geliştirme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bu bölüm yardımcı olacak konulara bağlantılar eski dil hizmeti oluşturun.  
  
 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Dil hizmeti uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [düzenleyici ve dil hizmeti uzantıları](../../extensibility/editor-and-language-service-extensions.md).  
  
> [!NOTE]
>  Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Eski Dil Hizmetinin Modeli](../../extensibility/internals/model-of-a-legacy-language-service.md)  
 Minimal dil hizmeti için modeli sağlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] çekirdek Düzenleyici. Bu model, kendi dil hizmeti oluşturmak için bir kılavuz olarak kullanabilirsiniz.  
  
 [Eski Dil Hizmeti Arabirimleri](../../extensibility/internals/legacy-language-service-interfaces.md)  
 Dil hizmeti uygulamak için gereken nesneleri açıklanır ve söz dizimi vurgulama, yöntem verileri ve diğer özellikleri sağlamak için kullanabileceğiniz ek nesnelerin bir listesini sağlar.  
  
 [Eski Dil Hizmeti Komutlarını Kesme](../../extensibility/internals/intercepting-legacy-language-service-commands.md)  
 Dil hizmetinize metin görünümünü aksi işlemek ıntercept komutları komut filtre eklemek açıklar.  
  
 [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service2.md)  
 Dil hizmetinizi kullanarak kaydetme hakkında bilgi sağlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].  
  
 [Hata Ayıklama için Dil Hizmeti Desteği](../../extensibility/internals/language-service-support-for-debugging.md)  
 Dil hizmeti bir hata ayıklayıcı destekleyecek şekilde süreçlerinizi nasıl sağlayabilirsiniz açıklar.  
  
 [Denetim listesi: Eski dil hizmeti oluşturma](../../extensibility/internals/checklist-creating-a-legacy-language-service.md)  
 Oluşturma ve çekirdek Düzenleyicisi için bir dil hizmeti tümleştirmek için adım adım yönergeler sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Eski Dil Hizmetinde Söz Dizimi Renklendirmesi](../../extensibility/internals/syntax-coloring-in-a-legacy-language-service.md)  
 Uygulama, dil hizmetinde söz dizimi vurgulama anlatılmaktadır.  
  
 [Eski Dil Hizmetinde Deyim Tamamlama](../../extensibility/internals/statement-completion-in-a-legacy-language-service.md)  
 Deyim tamamlama, bir dil anahtar sözcüğü veya yazarak başlatılan öğenin son kullanıcılara yardımcı olan tarafından bir dil hizmeti işlemi açıklanır.  
  
 [Eski Dil Hizmetinde Parametre Bilgileri](../../extensibility/internals/parameter-info-in-a-legacy-language-service1.md)  
 Aşırı yüklenmiş işlevlere ve metotlara için yöntemi ipuçları sağlanacağı anlatılmaktadır.  
  
 [Nasıl yapılır: Eski dil hizmetinde gizli metin desteği](../../extensibility/internals/how-to-provide-hidden-text-support-in-a-legacy-language-service.md)  
 Gizli metin alanının amacını ve gizli metin bölge ekleme hakkında yönergeler sağlar.  
  
 [Nasıl yapılır: Eski dil hizmetinde genişletilmiş ana hat oluşturma desteği sağlar](../../extensibility/internals/how-to-provide-expanded-outlining-support-in-a-legacy-language-service.md)  
 Ana hat oluşturma desteği destekleyen ötesinde dil genişleten iki seçenek açıklanır *tanımlara Daralt* komutu.
