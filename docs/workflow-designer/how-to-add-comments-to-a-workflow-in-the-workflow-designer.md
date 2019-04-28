---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: Bir iş akışına açıklama ekleme'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- System.Activities.Presentation.Annotations.Annotation.UI
- Annotation
ms.assetid: 9aa0e8d6-8129-4438-8389-d460611581a7
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: c7eb15c6d19ab40df6913dd67466dc20012492b7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950376"
---
# <a name="how-to-add-comments-to-a-workflow-in-the-workflow-designer"></a>Nasıl yapılır: İş Akışı Tasarımcısında bir iş akışına açıklama ekleme

Daha büyük, daha karmaşık iş akışları oluşturmayı kolaylaştırmak için .NET Framework 4.5 öğesi Tasarımcısı'nda aşağıdaki türden ek açıklamalar eklemek Geliştirici sağlar:

- <xref:System.Activities.Activity>

- <xref:System.Activities.Statements.State>

- <xref:System.Activities.Statements.Transition>

- Türetilmiş sınıflar <xref:System.Activities.Statements.FlowNode>

- <xref:System.Activities.Variable>

- <xref:System.Activities.Argument>

> [!IMPORTANT]
> Ek açıklamanın içeriğini iş akışıyla ilişkilendirilmiş XAML dosyasına düz metin olarak kaydedilir ve başkaları tarafından potansiyel olarak okunamadı. Bir ek açıklama hassas bilgileri girerek oluştururken dikkatli olun.

## <a name="adding-an-annotation-to-an-activity-in-the-designer"></a>Bir etkinlik Tasarımcısı'nda bir ek açıklama ekleme

1. İş Akışı Tasarımcısı'nda iş akışı Tasarımcısı ve seçim içindeki bir öğeyi sağ **ek açıklamaları**, **ek açıklama Ekle**.

1. Ek açıklamanın metin sağlanan alana ekleyin.

   Öğe bir ek açıklama simgesini gösterir. Ek açıklama simgenin üzerine geldiğinizde, ek açıklama metni görüntüler.

## <a name="displaying-an-annotation-in-an-activitys-designer"></a>Ek açıklamanın bir etkinliğin tasarımcıda görüntüleme

1. Bir ek açıklama dışında etkinlik görüntüleme olan bir etkinlik Tasarımcısı ile tıklayın **PIN** ek açıklama donatıcı simgesi.

   Ek açıklama etkinlik Tasarımcısı'nda görüntülenir. Aşağıdaki ekran görüntüsünde, ek açıklama "Başlangıç etkinliği iş akışı" etkinlik Tasarımcısı'nda görüntülenir.

   ![Etkinlik Tasarımcısı'nda gösterilen ek açıklaması](../workflow-designer/media/annotationindesigner.png)

2. Ek açıklama etkinlik Tasarımcısı dışında görüntülemek için etkinlik Tasarımcısı'nda ek açıklama alanı üzerine gelin ve tıklayın **Unpın** simgesi

   ![Ek açıklama görüntülenen dışında bir etkinlik Tasarımcısı](../workflow-designer/media/annotationoutsidedesigner.png)

## <a name="showing-or-hiding-all-annotations"></a>Tüm ek açıklamaları gizleme veya gösterme

1. Ek açıklamanın sahip bir etkinliğe sağ tıklayın. Seçin **ek açıklamaları**, **tüm ek açıklamaları Göster**.

   Tüm ek açıklamaları etkinliğin tasarımcılarda görüntülenir.

1. Etkinlik tasarımcıları dışında tüm ek açıklamaları görüntülemek için etkinliği sağ tıklatın ve **ek açıklamaları**, **tüm ek açıklamaları Gizle**.

## <a name="editing-or-deleting-an-annotation-for-an-activity"></a>Bir etkinlik için ek açıklamanın silinmesi veya düzenleme

1. Ek açıklamanın sahip bir etkinliği sağ tıklatın.

1. Seçin **ek açıklamaları**, **Düzenle ek açıklama** veya **açıklamayı Sil**.

   Ek açıklama düzenlenmek üzere açıldıktan ya da silinir.

1. Tüm ek açıklamaları tek seferde silmek için iş akışı Tasarımcısı ve select sağ **ek açıklama**, **tüm ek açıklamaları silme**.

## <a name="adding-editing-and-deleting-an-annotation-for-a-variable-or-argument"></a>Ekleme, düzenleme ve bir değişkene veya bağımsız bir ek açıklamayı silme

1. Bir değişken veya bağımsız değişken üzerinde sağ tıklayın ve ek açıklama Ekle'ı seçin.

1. Ek Açıklama metnini girin. Değişken veya bağımsız değişken bir ek açıklama simgesi görüntüler.

1. Bir değişkeni veya bir ek açıklama sahip bağımsız değişken üzerinde sağ tıklayın. Ek Açıklama Düzenle.

   Ek açıklama düzenleme için açılır.

1. Bir değişkeni veya bir ek açıklama sahip bağımsız değişken üzerinde sağ tıklayın. Ek Açıklama Sil'i seçin.

   Ek açıklama silindi.