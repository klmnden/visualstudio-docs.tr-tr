---
title: İş Akışı Tasarımcısı - TryCatch etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.TryCatch.UI
- System.Activities.Statements.Catch`1.UI
ms.assetid: 02a326c2-4009-442f-b7cb-e42121fd2992
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 079c25b2bbaa37432009f0eeade9673f8d0afd28
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433961"
---
# <a name="trycatch-activity-designer"></a>TryCatch Etkinlik Tasarımcısı

**TryCatch** etkinlik Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.TryCatch> etkinlik.

## <a name="the-trycatch-activity"></a>TryCatch etkinlik
 <xref:System.Activities.Statements.TryCatch> Etkinliği içeren bir <xref:System.Activities.Statements.TryCatch.Try%2A> etkinliği, koleksiyonu **Catch\<TException >** ve <xref:System.Activities.Statements.TryCatch.Finally%2A> etkinlik. A <xref:System.Activities.Statements.Catch%601> türü **TException** içeren bir <xref:System.Activities.Statements.Catch%601.ExceptionType%2A> ve <xref:System.Activities.Statements.Catch%601.Action%2A>. Birlikte işleme mekanizması tipik bir özel durum tabanlı hata uygulamak için kullanılırlar. A <xref:System.Activities.Statements.TryCatch> etkinlik çalıştığında yürütmek onun <xref:System.Activities.Statements.TryCatch.Try%2A> etkinlik. Varsa <xref:System.Activities.Statements.TryCatch.Try%2A> etkinlik hiçbir özel durum oluşturursa <xref:System.Activities.Statements.TryCatch> etkinliği kullanır, **Catch < TException\>**  özel durum eşleşmesi için koleksiyonu. Bir eşleşme varsa sonra <xref:System.Activities.Statements.Catch%601.Action%2A> karşılık gelen **Catch\<TException >** , hata işleme mantığı için özel olarak yürütülür. Etkinlikler, <xref:System.Activities.Statements.TryCatch.Try%2A> bölümü başarıyla tamamlanması veya etkinliklerinin <xref:System.Activities.Statements.TryCatch.Catches%2A> başarıyla tamamlanması <xref:System.Activities.Statements.TryCatch> etkinliği yürütür, <xref:System.Activities.Statements.TryCatch.Finally%2A> etkinlik. Daha fazla bilgi için [Windows iş akışı özel durumları](/dotnet/framework/windows-workflow-foundation/exceptions).

### <a name="using-the-trycatch-activity-designer"></a>TryCatch etkinlik Tasarımcısı kullanma

Erişim **TryCatch** etkinlik Tasarımcısı'nda **hata işleme** kategorisi **araç kutusu**.

**TryCatch** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde, gibi olarak içinde iş akışı Tasarımcısı yüzeyine açın bırakılan bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.TryCatch> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> TryCatch biri. <xref:System.Activities.Activity.DisplayName%2A> Değeri üst bilgisinde düzenlenebilir **TryCatch** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu. Diğer özellikler yüzeyine düzenlenmelidir **TryCatch** etkinlik Tasarımcısı.

Sağ üst köşesindeki genişletme düğmesine **TryCatch** görmek için tasarımcı **deneyin**, **yakalar**, ve **son** kutusu Genişletilmiş Görünüm. Bir catch eklemek için tıklatın **yeni catch ekleme** düğmesini **TryCatch** Tasarımcısı. Düğme türü açılan kutuya değiştirir. Bir özel durum türü seçin ve yakalama eklemek için ENTER tuşuna basın. Ekledikten sonra bir **Catch**, catch alanı genişler ve bir etkinlik yakalama yürütme mantığı tanımlamak için yakalama uygulamasına bırakılabilir. Genişletilmiş catch alanının sağ tarafında bir metin kutusu olduğuna dikkat edin. Bu metin kutusunu kullanarak özel durum değişkeninin adı verebilirsiniz. Özel durum değişkeni yalnızca aynı içindeki etkinlikler için kullanılabilir **Catch**.

**TryCatch** Tasarımcısı düzenlemeyi desteklemiyor **Catch**. Özel durum türü değiştirmek istiyorsanız, silmek sahip **Catch** ve yeni bir tane ekleyin. A **Catch** seçip silerek veya seçerek silinebilir **Sil** tıklanarak erişilen bağlam menüsünde.

### <a name="the-trycatch-properties"></a>TryCatch özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.TryCatch>özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|İsteğe bağlı kolay adı belirtir <xref:System.Activities.Statements.TryCatch> etkinlik. TryCatch varsayılandır.|
|<xref:System.Activities.Statements.TryCatch.Try%2A>|False|Etkinlik yürütülmesi ilk <xref:System.Activities.Statements.TryCatch> yürütür.|
|<xref:System.Activities.Statements.TryCatch.Catches%2A>|False|Koleksiyonu **Catch** , denetlenecek öğelerin <xref:System.Activities.Statements.TryCatch.Try%2A> etkinlik bir özel durum oluşturur.<br /><br /> En az bir etkinlik ekleyin <xref:System.Activities.Statements.TryCatch.Catches%2A> veya bir etkinlikte <xref:System.Activities.Statements.TryCatch.Finally%2A> blok.|
|<xref:System.Activities.Statements.TryCatch.Finally%2A>|False|Etkinlik zaman yürütülecek <xref:System.Activities.Statements.TryCatch.Try%2A> ve gerekli tüm etkinlikleri <xref:System.Activities.Statements.TryCatch.Catches%2A> koleksiyonu tam yürütme.<br /><br /> En az bir etkinlik ekleyin <xref:System.Activities.Statements.TryCatch.Catches%2A> veya bir etkinlikte <xref:System.Activities.Statements.TryCatch.Finally%2A> blok.|

## <a name="see-also"></a>Ayrıca bkz.

- [Koleksiyon](../workflow-designer/collection-activity-designers.md)
- [Rethrow](../workflow-designer/rethrow-activity-designer.md)
- [Throw](../workflow-designer/throw-activity-designer.md)