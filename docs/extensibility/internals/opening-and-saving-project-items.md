---
title: Açma ve proje öğelerini kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], file persistence
- files [Visual Studio], opening and saving
- editors [Visual Studio SDK], file persistence
ms.assetid: f71898ad-335f-4c43-a177-4da87078afd1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7ca83cb6d2913e0c0a91f4a6e874640ae57c7708
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602435"
---
# <a name="opening-and-saving-project-items"></a>Proje Öğelerini Açma ve Kaydetme
Yeni bir proje türü eklediğinizde, proje dosyalarınızı kaydetme ve açma yönetmelidir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE). Aşağıdaki konular, dosyaları açma ve kaydetme için farklı yaklaşımlara tartışın.

## <a name="in-this-section"></a>Bu Bölümde
- [Dosya Aç Komutunu Kullanarak Dosyaları Görüntüleme](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)

 Sunar IDE'nin nasıl işleyeceğini bir adım adım açıklama **açık dosya** komut ve bu komuta yanıt projeleri rolü.

- [Birlikte Aç Komutunu Kullanarak Dosyaları Görüntüleme](../../extensibility/internals/displaying-files-by-using-the-open-with-command.md)

 Sunar IDE'nin nasıl işleyeceğini bir ayrıntılı, adım adım açıklama **birlikte Aç** bazı standart düzenleyicileri, tercih ettiğiniz bir dosya açma isteyen komutu.

- [Nasıl yapılır: Projeye özgü düzenleyicileri açma](../../extensibility/how-to-open-project-specific-editors.md)

 Bir projeye özgü Düzenleyicisi'ni kullanarak belirli bir tür, projenizdeki dosyaları açılması gerektiğini belirtmek için adım adım yönergeler sağlar.

- [Nasıl yapılır: Open Standard Editors](../../extensibility/how-to-open-standard-editors.md)

 Dosyalar için standart bir düzenleyici proje türünüzü açmak IDE etkinleştirme belirtmek için adım adım yönergeler sağlar.

- [Nasıl yapılır: Açık açık belgeler için düzenleyicileri](../../extensibility/how-to-open-editors-for-open-documents.md)

 Açık bir dosya için bir projeye özgü düzenleyicisini açmak için adım adım yönergeler sağlar.

- [Standart Belge Kaydetme](../../extensibility/internals/saving-a-standard-document.md)

 IDE nasıl işlediğini ayrıntılı bir açıklama sağlar **Kaydet**, **Kaydet**, ve **Tümünü Kaydet** komutları bir belge için standart bir düzenleyicide açık.

- [Özel Belge Kaydetme](../../extensibility/internals/saving-a-custom-document.md)

 Bir diyagram ve IDE nasıl işlediğini konusunda ayrıntılı bilgi sağlar **Kaydet**, **Kaydet**, ve **Tümünü Kaydet** komutları belgeler için özel bir düzenleyicide açık.

- [Projedeki Bir Dosyayı Hangi Düzenleyicinin Açacağını Belirleme](../../extensibility/internals/determining-which-editor-opens-a-file-in-a-project.md)

 Uygun Düzenleyici ya da bir dosya için tasarımcı seçmek için IDE'yi izlediği süreç ele alınmaktadır.

## <a name="related-sections"></a>İlgili Bölümler
- [Özel Düzenleyiciler ve Tasarımcılar Oluşturma](../../extensibility/creating-custom-editors-and-designers.md)

 IDE barındırabilir ve tanımlarını her düzenleyicinin verir düzenleyicileri dört türlerini listeler.

- [Proje Türleri](../../extensibility/internals/project-types.md)

 Proje öğeleri nasıl biçimlendirileceğini nasıl projeleri kod derlenmiş ve yerleşik denetlenmesine ve düzenleyicileri nasıl açıldığı gibi ele alınmaktadır.