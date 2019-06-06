---
title: 'İş Akışı Tasarımcısı: System.Activities, araç kutusu öğelerini Seç'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- VS.CHOOSEITEMS.SYSTEM.ACTIVITIES_COMPONENTS
- VS.CHOOSEITEMS.SYSTEM.ACTIVITIES COMPONENTS
ms.assetid: cef390cd-eeda-42e6-9d2e-18c8325a4f06
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fd25b939519bb1a1cb179ab5bbd4d20b9307f920
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747763"
---
# <a name="systemactivities-tab-choose-toolbox-items-dialog-box"></a>System.Activities sekmesi, araç kutusu öğelerini Seç iletişim kutusu

Bu sekme, **araç kutusu öğelerini Seç** iletişim kutusu, Windows Workflow Foundation (WF) etkinlikleri, şablonları ve kullanılabilir öğeleri listesini görüntüler. Bu listeyi görüntülemek için seçin **araç kutusu öğelerini Seç** gelen **Araçları** menüsü veya sağ tıklayarak **araç kutusu** seçerek **öğelerini Seç**görüntülenecek **araç kutusu öğelerini Seç** iletişim kutusunu ve ardından kendi **System.Activities** sekmesi. Kullanıma hazır, liste iş akışı etkinlikleri System.Activities System.ServiceModel.Activities ve System.Activities.Core.Presentation derlemelerden içerir. Ancak, yalnızca sistem tarafından sağlanan gösterilen etkinlikleri ve görüntülenen diğer derlemeleriyle eklenen etkinlikleri **araç kutusu** varsayılan olarak denetlenir. En son eklenen etkinlikler otomatik olarak denetlenir ve görünür **araç kutusu** tıkladığınızda **Tamam** iletişim kutusundaki. Bu öğeler de görünür **araç kutusu** etkinlik/öğe/şablonunda yer aldığı ad alanına karşılık gelen yeni bir kategori altında.

> [!WARNING]
> Herhangi bir iş akışı etkinlik içermiyor bir bütünleştirilmiş kod eklemeyi denerseniz, derleme hiç etkinlik içermiyor açıklayan bir hata iletişim kutusu görüntülenir.

Bu iletişim kutusunda proje belirsiz olduğundan ve bu nedenle **System.Activities** sekmesini tek başına XAML ya da bir iş akışı dışın proje türü görünmesini devam eder.

Filtreleme her sekmede gerçekleştirilir ve iş akışı etkinlikleri aracılığıyla eklemek mümkün değildir **.NET bileşeni** sekmesi. Bloblarda ekleme **System.Activities** kendisini sekmesi.

Tüm öğeleri görmek için istemediğiniz işaretini kaldırarak **araç kutusu** bu iletişim kutusundan sekmesinde veya alternatif olarak, bunu kullanarak yapabilirsiniz **Sil** menü seçeneğini sağ tıklayın **araç kutusu**ve serbest bir derlemeye başvuran öğesinden kaldırmaz **araç kutusu**.

Tasarımcıda bırakarak etkinlik örnekleme başvurulan bütünleştirilmiş kodların listesi öğesine otomatik olarak içeren derlemeyi ekler. Etkinlik derleme C başvuruyorsa, ayrıca, C başvurulan derleme listesine eklemez. C derlemeyi GAC'ye veya etkinlik b ile aynı dizinde olması gerekir Tek başına durumda, derlemeyi GAC veya VS araştırma yollarını olması gerekir. Ancak bundan sonra sürükleyip bırakabilirsiniz etkinlik iş akışı Tasarımcı yüzeyinde.

**Araç kutusu** ayarları kullanıcı seçenekleri varsayılan olarak kaydedileceği böylece olduğunda, sonraki açışınızda, **araç kutusu**, özelleştirilmiş iş akışı etkinlikleri listesini görüntüler. Bu bir yan etkisi olan, belirli bir etki alanı öğelerinizi eklediyseniz **araç kutusu** aracılığıyla **araç kutusu öğelerini Seç** iletişim kutusu, yine de devam, çalışırken bu öğeleri görmek bir De iş akışı konsol uygulaması. Bunları görmek istemiyorsanız, sonra sağ tıklama menüsünü kullanarak bunları silin veya aracılığıyla işaretini kaldırın **araç kutusu öğelerini Seç** daha önce belirtildiği gibi iletişim kutusu.

Sütunları bu iletişim kutusunda aşağıdaki bilgileri içerir:

Name\
Yerel makinenizde şu anda kayıtlı olan iş akışı etkinlikleri adlarını listeler.

Namespace\
Etkinlik yapısını tanımlar .NET ad alanı hiyerarşisini görüntüler.

Derleme Name\
Etkinlik içeren .NET derleme sürümünü ve adını görüntüler.

Directory\
İş akışı etkinlikleri içeren .NET derleme konumunu görüntüler. Genel Derleme Önbelleği tüm derlemeler için varsayılan konumdur.

Listelenen bileşenleri sıralamak için herhangi bir sütun başlığını seçin.