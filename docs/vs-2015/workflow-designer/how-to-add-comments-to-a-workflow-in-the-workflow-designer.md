---
title: 'Nasıl yapılır: İş akışı tasarımcısında bir iş akışı aracılığıyla açıklama ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.Annotations.Annotation.UI
- Annotation
ms.assetid: 9aa0e8d6-8129-4438-8389-d460611581a7
caps.latest.revision: 7
author: steved0x
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f826168d3b198090ba58f409f096b4b12c760c70
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60059675"
---
# <a name="how-to-add-comments-to-a-workflow-in-the-workflow-designer"></a>Nasıl yapılır: İş Akışı Tasarımcısında bir iş akışına açıklama ekleme
Daha büyük, daha karmaşık iş akışları oluşturma kolaylaştırmak için [!INCLUDE[net_v45](../includes/net-v45-md.md)] öğesi Tasarımcısı'nda aşağıdaki türden ek açıklamalar eklemek geliştiricinin sağlar:  
  
- <xref:System.Activities.Activity>  
  
- <xref:System.Activities.Statements.State>  
  
- <xref:System.Activities.Statements.Transition>  
  
- Türetilmiş sınıflar <xref:System.Activities.Statements.FlowNode>  
  
- <xref:System.Activities.Variable>  
  
- <xref:System.Activities.Argument>  
  
> [!IMPORTANT]
>  Ek açıklamanın içeriğini iş akışıyla ilişkilendirilmiş XAML dosyasına düz metin olarak kaydedilir ve başkaları tarafından potansiyel olarak okunamadı. Bir ek açıklama hassas bilgileri girerek oluştururken dikkatli olun.  
  
### <a name="adding-an-annotation-to-an-activity-in-the-designer"></a>Bir etkinlik Tasarımcısı'nda bir ek açıklama ekleme  
  
1. İş Akışı Tasarımcısı'nda iş akışı Tasarımcısı ve seçim içindeki bir öğeyi sağ **ek açıklamaları**, **ek açıklama Ekle**.  
  
2. Ek açıklamanın metin sağlanan alana ekleyin.  
  
3. Öğe bir ek açıklama simgesi gösterilir. Ek açıklama simgenin üzerine geldiğinizde, ek açıklama metni görüntülenir.  
  
     ![Sıralı etkinlik ek açıklama gösteren](../workflow-designer/media/annotation.png "ek açıklaması")  
  
### <a name="displaying-an-annotation-in-an-activitys-designer"></a>Ek açıklamanın bir etkinliğin tasarımcıda görüntüleme  
  
1. Bir ek açıklama dışında etkinlik görüntüleme olan bir etkinlik Tasarımcısı ile tıklayın **PIN** ek açıklama donatıcı simgesi.  
  
2. Ek açıklama etkinlik Tasarımcısı'nda görüntülenir. Aşağıdaki ekran görüntüsünde, ek açıklama "Başlangıç etkinliği iş akışı" etkinlik Tasarımcısı'nda görüntülenir.  
  
     ![Etkinlik Tasarımcısı'nda gösterilen ek açıklama](../workflow-designer/media/annotationindesigner.png "AnnotationInDesigner")  
  
3. Ek açıklama etkinlik Tasarımcısı dışında görüntülemek için etkinlik Tasarımcısı'nda ek açıklama alanı üzerine gelin ve tıklayın **Unpın** simgesi  
  
     ![Ek açıklama dışında bir etkinliğin designe görüntülenen](../workflow-designer/media/annotationoutsidedesigner.png "AnnotationOutsideDesigner")  
  
### <a name="showing-or-hiding-all-annotations"></a>Tüm ek açıklamaları gizleme veya gösterme  
  
1. Ek açıklamanın sahip bir etkinliğe sağ tıklayın. Seçin **ek açıklamaları**, **tüm ek açıklamaları Göster**.  
  
2. Tüm ek açıklamaları etkinliğin tasarımcılarda görüntülenir.  
  
3. Etkinlik tasarımcıları dışında tüm ek açıklamaları görüntülemek için etkinliği sağ tıklatın ve **ek açıklamaları**, **tüm ek açıklamaları Gizle**.  
  
### <a name="editing-or-deleting-an-annotation-for-an-activity"></a>Bir etkinlik için ek açıklamanın silinmesi veya düzenleme  
  
1. Ek açıklamanın sahip bir etkinliği sağ tıklatın.  
  
2. Seçin **ek açıklamaları**, **Düzenle ek açıklama** veya **açıklamayı Sil**.  
  
3. Ek açıklama düzenlenmek üzere açıldıktan veya silindi.  
  
4. Tüm ek açıklamaları tek seferde silmek için iş akışı Tasarımcısı ve select sağ **ek açıklama**, **tüm ek açıklamaları silme**.  
  
### <a name="adding-editing-and-deleting-an-annotation-for-a-variable-or-argument"></a>Ekleme, düzenleme ve bir değişkene veya bağımsız bir ek açıklamayı silme  
  
1. Bir değişken veya bağımsız değişken üzerinde sağ tıklayın ve ek açıklama Ekle'ı seçin.  
  
2. Ek Açıklama metnini girin. Değişken veya bağımsız değişken bir ek açıklama simgesi görüntüler.  
  
3. Bir değişkeni veya bir ek açıklama sahip bağımsız değişken üzerinde sağ tıklayın. Ek Açıklama Düzenle.  
  
4. Ek açıklama düzenleme için açılır.  
  
5. Bir değişkeni veya bir ek açıklama sahip bağımsız değişken üzerinde sağ tıklayın. Ek Açıklama Sil'i seçin.  
  
6. Ek açıklama silinir.