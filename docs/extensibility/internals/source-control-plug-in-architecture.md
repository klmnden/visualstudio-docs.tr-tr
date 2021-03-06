---
title: Kaynak Denetimi Eklentisi mimarisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, architecture
ms.assetid: 35351d4c-9414-409b-98fc-f2023e2426b7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 75b283a2013b67b28d90ba8a47dbee41cae1f848
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322537"
---
# <a name="source-control-plug-in-architecture"></a>Kaynak Denetimi Eklentisi Mimarisi
İçin kaynak denetimi desteği ekleyebilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE) ile uygulama ve kaynak denetimi eklentisi ekleniyor. IDE kaynak denetimi eklentisi iyi tanımlanmış kaynak denetimi eklentisi API aracılığıyla bağlanır. IDE, araç çubuklarını ve menü komutları oluşan bir kullanıcı arabirimi (UI) sağlayarak kaynak denetim sistemi sürüm denetimi özellikleri sunar. Kaynak Denetimi Eklentisi, kaynak denetim işlevselliğini uygular.

## <a name="source-control-plug-in-resources"></a>Kaynak denetimi eklentisi kaynakları
 Kaynak Denetimi Eklentisi oluşturma ve bu sürüm uygulamanıza yardımcı olacak kaynaklar sunulmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE. Kaynak Denetimi Eklentisi API belirtimine kaynak denetimi eklentisi tarafından uygulanması gerekir ve böylece içine tümleştirilebilir içeren [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE. Ayrıca uygulayan bir çatı kaynak denetimi eklentisi gösteren uygulaması kaynak denetimi eklentisi API ile uyumlu temel işlevleri (C++ ile yazılmış) bir kod örneği içerir.

 Kaynak Denetimi Eklentisi API belirtimine uygun olarak kaynak denetimi eklentisi API uygulanan işlevleri gerekli kümesi ile bir kaynak denetim DLL oluşturursanız, tercih ettiğiniz herhangi bir kaynak denetim sistemi yararlanmanıza olanak tanır.

## <a name="components"></a>Bileşenler
 Kaynak denetimi bağdaştırıcısı paketi diyagramda, kullanıcının istek için kaynak denetimi eklentisi tarafından desteklenen bir işlev çağrısının içine bir kaynak denetimi işlemi çeviren IDE bileşenidir. Bunun yapılması, IDE ve kaynak denetimi eklentisi bilgileri IDE ve eklentinin arasında ileri ve geri geçirir verimli bir iletişim kutusu olmalıdır. Bu iletişim gerçekleşmesi, her ikisi de aynı dili konuşan gerekir. Bu belgede özetlenen kaynak denetimi eklentisi API bu bir alışverişi için ortak Sözlüğü ' dir.

 ![Kaynak kodu denetimi mimarisi diyagramı](../../extensibility/internals/media/vs_sccsdk_plug_in_arch.gif "vs_sccsdk_plug_in_arch") mimarisi arasındaki etkileşimler VS ve kaynak denetimi eklentisi gösteren diyagram

 Mimari diyagramında gösterildiği [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] VS shell diyagramdaki olarak etiketlenmiş shell barındıran kullanıcının çalışma projeler ve düzenleyiciler ve Çözüm Gezgini gibi ilişkili bileşenleri. Kaynak denetimi bağdaştırıcısı paketi IDE ve kaynak denetimi eklentisi arasındaki etkileşimi işler. Kaynak denetimi bağdaştırıcısı paketi kendi kaynak denetimi kullanıcı Arabirimi sağlar. Buna kullanıcının başlatmak ve kaynak denetimi işlemi kapsamını tanımlamak için etkileşime en üst düzey bir kullanıcı Arabirimi var.

 Kaynak Denetimi Eklentisi, şekilde gösterildiği gibi iki bölümden oluşur, kendi kullanıcı Arabirimi olabilir. "Satıcı kullanıcı Arabirimi" etiketli kutunun seçili olduğunu, sağladığınız kaynak denetimi eklentisi oluşturucusu olarak, özel kullanıcı arabirimi öğelerini temsil eder. Kullanıcı bir Gelişmiş kaynak denetimi işlemi çalıştırdığında bunlar doğrudan kaynak denetimi eklentisi tarafından gösterilir. "Yardımcısı kullanıcı Arabirimi" etiketli kutunun seçili olduğunu IDE üzerinden dolaylı olarak çağrılan kaynak denetimi eklentisi kullanıcı Arabirimi özellikleri kümesidir. Kaynak Denetimi Eklentisi IDE tarafından sağlanan özel geri çağırma işlevleri aracılığıyla IDE kullanıcı Arabirimi-ilgili iletiler geçirir. IDE ile daha sorunsuz bir tümleştirme UI Yardımcısı kolaylaştırır (genellikle kullanımının bir **Gelişmiş** düğme) ve bu nedenle daha birleştirilmiş bir son kullanıcı deneyimi sağlar.

 Kaynak denetimi eklentisi için değişiklik yapamaz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kabuk ve sonuç olarak, IDE tarafından sağlanan kullanıcı Arabirimi için kaynak denetimi bağdaştırıcısı paketi veya kaynak denetimi. Bu uygulama son kullanıcı için tümleşik bir deneyim için katkıda bulunan çeşitli kaynak denetimi eklentisi API işlevleri aracılığıyla sunulan esnekliği maksimum kullanım yapmanız gerekir. Kaynak Denetimi Eklentisi API belgeleri başvuru bölümü, bazı gelişmiş kaynak denetimi eklentisi özellikleri için bilgileri içerir. Bu özelliklerden yararlanmak için kaynak denetimi eklentisi başlatma sırasında gelişmiş özelliklerini IDE bildirmeniz gerekir ve her özellik için belirli gelişmiş işlevleri uygulamalıdır.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentileri](../../extensibility/source-control-plug-ins.md)
- [Sözlük](../../extensibility/source-control-plug-in-glossary.md)
- [Kaynak Denetimi Eklentisi Oluşturma](../../extensibility/internals/creating-a-source-control-plug-in.md)