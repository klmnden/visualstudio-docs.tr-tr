---
title: Çalışma zamanında Şerite erişin
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Globals class, Ribbon
- Ribbon [Office development in Visual Studio], accessing
- RibbonManager class
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7c7fdda6234f1e98117cdb1bf047762ed9d4621a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255738"
---
# <a name="access-the-ribbon-at-run-time"></a>Çalışma zamanında Şerite erişin
  Şeriti göstermek, gizlemek ve değiştirmek için kod yazabilir ve kullanıcıların kodu özel bir görev bölmesinde, Eylemler bölmesinde veya Outlook form bölgesindeki denetimlerden çalıştırmasını sağlayabilirsiniz.

 `Globals` Sınıfını kullanarak şerit 'e erişebilirsiniz. Outlook projeleri için, belirli bir Outlook denetçisinde veya Outlook Explorer penceresinde görünen Şeritlere erişebilirsiniz.

 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]

## <a name="access-the-ribbon-by-using-the-globals-class"></a>Globals sınıfını kullanarak şeride erişin
 Belge düzeyindeki bir projede `Globals` veya VSTO eklenti projesindeki şerit 'e, projenin herhangi bir yerinden erişmek için sınıfını kullanabilirsiniz.

 `Globals` Sınıfı hakkında daha fazla bilgi için bkz. [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md).

 Aşağıdaki örnek, adlı `Globals` `Ribbon1` özel bir Şerite erişmek ve Şeritteki Birleşik giriş `Hello World`kutusunda görüntülenen metni ayarlamak için sınıfını kullanır.

 [!code-vb[Trin_Outlook_FR_Access#4](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#4)]
 [!code-csharp[Trin_Outlook_FR_Access#4](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#4)]

## <a name="access-a-collection-of-ribbons-that-appear-in-a-specific-outlook-inspector-window"></a>Belirli bir Outlook Inspector penceresinde görünen Şerit koleksiyonuna erişin
 Outlook *Inspector*' da görünen bir Şerit koleksiyonuna erişebilirsiniz. Inspector, kullanıcılar e-posta iletileri oluşturma gibi belirli görevleri gerçekleştirirken Outlook 'ta açılan bir penceredir. Inspector penceresinin Şeritine erişmek için, `Ribbons` `Globals` sınıfının özelliğini çağırın ve denetçisi temsil eden bir <xref:Microsoft.Office.Interop.Outlook.Inspector> nesneyi geçirin.

 Aşağıdaki örnek, şu anda odağa sahip olan Inspector 'ın şerit koleksiyonunu alır. Bu örnek daha sonra adlı `Ribbon1` bir Şerite erişir ve `Hello World`Şeritteki Birleşik giriş kutusunda görüntülenen metni ayarlar.

 [!code-vb[Trin_Outlook_FR_Access#5](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#5)]
 [!code-csharp[Trin_Outlook_FR_Access#5](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#5)]

## <a name="access-a-collection-of-ribbons-that-appear-for-a-specific-outlook-explorer"></a>Belirli bir Outlook Gezgini için görüntülenen Şerit koleksiyonuna erişin
 Outlook *Explorer*'Da görünen Şerit koleksiyonuna erişebilirsiniz. Gezgin bir Outlook örneği için ana uygulama kullanıcı arabirimi (UI) ' dir. Gezgin penceresinin Şeritine erişmek için, `Ribbons` `Globals` sınıfının özelliğini çağırın ve Gezgini temsil eden bir <xref:Microsoft.Office.Interop.Outlook.Explorer> nesneyi geçirin.

 Aşağıdaki örnek, şu anda odağa sahip olan gezgin 'in şerit koleksiyonunu alır. Bu örnek daha sonra adlı `Ribbon1` bir Şerite erişir ve `Hello World`Şeritteki Birleşik giriş kutusunda görüntülenen metni ayarlar.

 [!code-vb[Trin_Outlook_FR_Access#6](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#6)]
 [!code-csharp[Trin_Outlook_FR_Access#6](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#6)]

## <a name="see-also"></a>Ayrıca bkz.
- [Şerite Genel Bakış](../vsto/ribbon-overview.md)
- [Şerit Tasarımcısı](../vsto/ribbon-designer.md)
- [Şerit XML](../vsto/ribbon-xml.md)
- [Şerit nesne modeline genel bakış](../vsto/ribbon-object-model-overview.md)
- [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)
- [İzlenecek yol: Çalışma zamanında Şeritteki denetimleri güncelleştirme](../vsto/walkthrough-updating-the-controls-on-a-ribbon-at-run-time.md)
- [Outlook için şerit özelleştirme](../vsto/customizing-a-ribbon-for-outlook.md)
- [Çalışma zamanında form bölgesine erişme](../vsto/accessing-a-form-region-at-run-time.md)
