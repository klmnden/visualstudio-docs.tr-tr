---
title: T4 Metin Dönüştürmeyi Özelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- text templates, API
- text templates, custom hosts
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: bc59718131cc4879a351097b767fa513d72b5c81
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962764"
---
# <a name="customize-t4-text-transformation"></a>T4 Metin Dönüştürmeyi Özelleştirme

Metin şablonları, Visual Studio'nun program kodu veya bir dönüştürme işlemiyle diğer metin dosyaları oluşturmanıza olanak tanıyan bir özelliktir. Kullanarak [!INCLUDE[vssdk_current_short](../modeling/includes/vssdk_current_short_md.md)], metin şablonu yönerge işlemcisini veya metin şablonu ana bilgisayarı'nı özelleştirerek varsayılan şablonu dönüştürme süreci genişletebilirsiniz.

## <a name="in-this-section"></a>Bu Bölümde

 [Metin şablonu dönüştürme süreci](../modeling/the-text-template-transformation-process.md) metin dönüştürmenin nasıl çalıştığını açıklar ve şablonu ana bilgisayarı ve yönerge işlemcilerine rolünü açıklar.

 [Özel T4 metin şablonu yönerge işlemcileri oluşturma](../modeling/creating-custom-t4-text-template-directive-processors.md) gibi yönerge işlemcisi, şablonunuzda yönergeleri ile ilgilenen `<#@template#>.` şablon derlenirken çalışır ve derlemeleri ve diğer kaynakları yükleyebilirsiniz. Ayrıca, çalışma zamanında kaynakları yükleyecek kod da ekleyebilirsiniz. Yönerge işlemciniz tanımlayarak şablonlarınızı karmaşıklığını azaltabilir.

 [Bir VS uzantısında metin dönüştürmeyi çağırma](../modeling/invoking-text-transformation-in-a-vs-extension.md) bir menü komutu veya olay işleyicisi gibi Visual Studio uzantısı yazıyorsanız, uzantınızı metin şablonu oluşturma hizmetini herhangi bir metin şablonu dönüştürmek için kullanabilirsiniz. Oturum nesnesi kullanarak şablona parametre verileri aktarmak ve değerleri şablon içinde almak `<#@parameter#>` yönergesi.

 [Bir özel konak kullanarak metin şablonlarını işleme](../modeling/processing-text-templates-by-using-a-custom-host.md) metin şablonunun kod yürütüldüğünde, ana dış dosyaları ve uygulama durumunu erişim sağlar. Örneğin, Visual Studio'da metin dönüştürmeleri çalıştıran konağa erişim sağlayabilir **Çözüm Gezgini**. Ayrıca hatalar hata iletisi penceresinde görüntüler. Farklı bir bağlamda metin dönüştürmeleri çalıştırmak istiyorsanız, bu bağlamda kullanılamayan hizmetlerine erişim sağlayan kendi ana tanımlayabilirsiniz.

 Visual Studio uzantısı yazıyorsanız, kendi ana bilgisayarınızı yazmak yerine var olan metin dönüştürme hizmetini kullanmayı göz önünde bulundurun. Daha fazla bilgi için [bir VS uzantısında metin dönüştürmeyi çağırma](../modeling/invoking-text-transformation-in-a-vs-extension.md).

## <a name="reference"></a>Başvuru

- [T4 metin şablonu yazma](../modeling/writing-a-t4-text-template.md) metin şablonu yönergeleri ve denetim blokları söz dizimi sağlar.