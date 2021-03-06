---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: İçerik Haritalı Gezinmeyi Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4a688056-37dc-406a-9071-be2141e192fe
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: de1004dd7a62fe4163147db4928783dd9a0dca98
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62949506"
---
# <a name="how-to-use-breadcrumb-navigation"></a>Nasıl yapılır: İçerik Haritalı Gezinmeyi Kullanma

İş Akışı Tasarımcısı'nda görüntülenen etkinlikler kümesini değiştirmek için üç ana yolu vardır:

1. Bir alt etkinlik ayrıntılarına girmek çift tıklayın.

2. Bir üst etkinliğe gitmek için içerik haritası çubuğundaki bir düğmeye tıklayın.

3. Genişletme veya daraltma yerinde etkinlikler.

## <a name="using-breadcrumb-navigation"></a>İçerik haritası gezintisini kullanma

1. Tıklandı etkinliği Kök etkinlik değiştirmek için iş akışı Tasarımcısı'nın bir etkinliğe çift tıklayın. Tıklandı etkinlik sonra tam kök dizininde genişletilir ve alt öğelerinden içerik haritası çubuğunda gösterilir. Bu durum bazen içinde veya dışında bir etkinlik ayrıntılara denir.

2. Geçerli Kök etkinlik öğesinin üst öğesi için gitmek için içerik haritası çubuğundaki etkinliği tıklatın.

## <a name="expanding-or-collapsing-an-activity-in-place"></a>Genişletme veya daraltma yerinde bir etkinlik

1. Bir etkinlik köşeli çift tıklayarak genişletir veya daraltır. etkinliği yerinde.

2. Düğmeye tıklayarak durumu genişletme durumu değiştirildiğinde, yeni genişletme durumunu XAML içinde kaydedilir.

    > [!WARNING]
    > Tüm etkinlikleri yerinde genişletilebilir. İki durum vardır etkinlik yerinde genişletildiğinde: ya da etkinliğin üst alt yerinde genişletilecek izin vermez, (örneğin, bir akış etkinlikleri yerinde genişletilemez), veya etkinlik Tasarımcısı kendisine izin vermiyor yerinde genişletilebilir. Hiçbir iş akışı Tasarımcısı'nda bulunan etkinlik tasarımcıları ikinci davranışa sahip olsa da, bazı özel etkinlikleri bu davranışı düşebilir.

## <a name="expanding-all-or-collapsing-all-activities"></a>Tüm genişletme veya daraltma tüm etkinlikler

1. Kullanım **Tümünü Genişlet** ve **Daralt tüm** genişletmek veya geçerli içerik haritası kökü altındaki etkinliklerin tümünü daraltmak için kullanıcı arabiriminde düğmeleri. Tümünü Genişlet ve Tümünü Daralt Not genel durumlarını aynıdır. Bu'ye kadar zaman içerik haritalı gezinme, Tümünü Genişlet kullanarak Kök etkinlik değiştirmek veya tüm durum Daralt kalıcı olduğu anlamına gelir **geri**.

2. Tüm genişletme uyguladığınız veya tüm durum Daralt sonra tıklayabilirsiniz **geri** her etkinliğe daha önce uyguladığınız durumu bakarak için geri dönmek için görüntülenen düğme.

    > [!WARNING]
    > Bir etkinlik ise gibi <xref:System.Activities.Statements.Flowchart>, ettikten dışında bir yerde genişletin, işlevselliği ile ilişkili **Tümünü Genişlet** ve **Tümünü Daralt** düğmeleri devre **akış çizelgesi**  Tasarımcısı. Hakkında daha fazla bilgi için **akış** Tasarımcı, bkz: [akış](../workflow-designer/flowchart-activity-designer.md) konu.

    > [!WARNING]
    > Tümünü Genişlet de sahip bir özel efekt **anahtar** ve **TryCatch** etkinlik tasarımcıları. Tıkladığınızda **Tümünü Genişlet**, tüm anahtar durumlarında ve try/catch/finally bloğu görüntülenir. Tıklayarak **geri** veya **Tümünü Daralt** bu tasarımcıları içinden tıklayabilirsiniz varsayılan durumlarına, bir tek çalışması/içeriğini görüntülemek için bloğu döndüren.