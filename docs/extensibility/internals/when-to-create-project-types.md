---
title: Proje türleri oluşturma zamanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project types, conditions for creating
ms.assetid: 26adc860-ee4a-4f5c-95e1-e41b207dd7e6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8be01ef0592deab48d923828ccfd3f86f1311a4d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323058"
---
# <a name="when-to-create-project-types"></a>Proje Türlerinin Oluşturulacağı Durumlar
Yeni bir proje türü oluşturmayı sağlayan temel özelleştirmek için [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kullanıcılarınız için. Ancak, yeni bir proje türü oluşturmak için tüm gerekli değildir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] özelleştirmeler. Aşağıdaki yönergeler, yeni bir proje türü senaryonuz için gerekli olup olmadığını belirlemenize yardımcı olmalıdır.

## <a name="create-a-new-project-type"></a>Yeni bir proje türü oluştur
 Özelleştirmek istiyorsanız, bir proje türü oluşturmalısınız [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] bir veya daha fazla aşağıdaki yollardan biriyle davranacak şekilde:

- Yapıya katılan, dağıtım, yapılandırmaları ve kaynak denetimi.

- Hata ayıklama desteği sunar.

- Proje öğeleri görüntülemek **Çözüm Gezgini**.

- Kullanım **Proje Aç** veya **yeni proje** iletişim kutusu.

- Proje iç içe geçirmeyi destekler.

## <a name="extend-an-existing-project-type"></a>Mevcut bir proje türünü genişletme
 Kullanabileceğiniz yeni bir proje türü oluşturmak isteyebilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] değiştirin veya varolan bir proje türünü davranışını genişletmek için aşağıdaki yollarla, örneğin, yapı işlemi için değiştirme [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] projeleri:

- Birden çok dosya ile tek bir birim olarak çalışır.

- Tek bir dosya alt öğelerinin bir hiyerarşi görüntüler.

- Bir komut içerik düzenleyicileri geçici olarak görüntüler.

- Hizmet bağlamı için düzenleyicileri görüntüler.

## <a name="use-an-existing-project-type"></a>Mevcut bir proje türünü kullanın.
 Yeni proje oluşturma bazen gerekli değildir. Aşağıdaki tabloda bir proje türü için oluşturmak zorunda değilsiniz görevler gösterilmektedir.

|Görev|Açıklama|
|----------|-----------------|
|Komutları işleme|Herhangi bir VSPackage komutları işleyebilir.|
|Bir düzenleyici oluşturma|Özel düzenleyicilerde kaydedilebilir. Daha fazla bilgi için [belge Windows ve düzenleyicileri](https://msdn.microsoft.com/library/603625e1-62b6-413a-bc44-089346e166bc).|
|Sahip olan Windows|Yeni bir proje türü eklemeden, hem araç ve belge pencereleri oluşturabilirsiniz.|
|Özellikler penceresinde özelliklerini gösterme|Tüm nesneleri özellikler getirebilir.|

## <a name="create-a-project-subtype"></a>Proje alt türü oluşturma
 Proje alt türleri, yeni bir proje türünüzü oluşturmak zorunda kalmadan bir yönetilen proje türü genişletmek için kullanabilirsiniz. Proje alt türleri, Microsoft yazılan yönetilen projeleri genişletmek için COM toplama kullanın [!INCLUDE[vbprvb](../../code-quality/includes/vbprvb_md.md)] veya [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)]. COM toplama, yönetilen proje sistemi uygulaması çoğunu yeniden kullanmak ve toplama ve kullanım arabirimleri destekleyen aracılığıyla belirli bir senaryo için yine de özelleştirebilirsiniz. Proje alt türleri hakkında daha fazla bilgi için bkz: [proje alt türleri](../../extensibility/internals/project-subtypes.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [Belge Windows ve düzenleyiciler](https://msdn.microsoft.com/library/603625e1-62b6-413a-bc44-089346e166bc)
- [Yapılacaklar listesi: Yeni Proje Türleri Oluşturma](../../extensibility/internals/checklist-creating-new-project-types.md)
- [Visual Studio’da Hiyerarşiler](../../extensibility/internals/hierarchies-in-visual-studio.md)