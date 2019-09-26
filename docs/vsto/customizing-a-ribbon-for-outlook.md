---
title: Outlook için şerit özelleştirme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Inspectors [Office development in Visual Studio]
- Outlook [Office development in Visual Studio], Ribbon
- customizing the Ribbon, about customizing the Ribbon
- custom Ribbon, about customizing the Ribbon
- Ribbon [Office development in Visual Studio], Outlook
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 646192baa6caaa33410b1dd8d17d1983f7d27e30
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255545"
---
# <a name="customize-a-ribbon-for-outlook"></a>Outlook için şerit özelleştirme
  Microsoft Office Outlook 'ta Şeriti özelleştirdiğinizde, özel şeritlerinizin uygulamada nerede görüneceğini göz önünde bulundurmanız gerekir. Outlook, ana uygulama kullanıcı arabiriminde (UI) ve kullanıcılar e-posta iletileri oluşturma gibi belirli görevleri gerçekleştirirken açık olan Windows 'da şeridi görüntüler. Bu uygulama pencereleri Inspectors olarak adlandırılmıştır.

 ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yaparım?: Outlook 'taki şeridi özelleştirmek için şerit tasarımcısını kullanın? ](http://go.microsoft.com/fwlink/?LinkID=130312).

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="add-a-custom-ribbon-to-the-main-application-ui"></a>Ana uygulama kullanıcı arabirimine özel bir şerit ekleme
 Outlook 'ta ana uygulama kullanıcı arabirimine gezgin denir. **Şerit (görsel Tasarımcı)** öğesini kullanıyorsanız, **Özellikler** penceresinde şeridin **RibbonType** özelliğine tıklayıp ardından **Microsoft. Outlook. Explorer**' ı seçerek gezgin 'e bir şerit ekleyebilirsiniz.

## <a name="assign-a-ribbon-to-an-inspector"></a>Bir Inspector 'a şerit atama
 Inspector için ileti sınıfına karşılık gelen Şerit türünü belirterek özelleştirmek istediğiniz Inspector 'ı belirlersiniz.

 **Şerit (görsel Tasarımcı)** öğesini kullanıyorsanız, **Özellikler** penceresinde şeridin **RibbonType** özelliğine tıklayın ve ardından değerler listesinden bir veya daha fazla şerit kimliği seçin.

 Projeye birden fazla şerit ekleyebilirsiniz. Birden fazla şerit bir Şerit kimliğini paylaşıyorsa, çalışma zamanında hangi Şeritin görüntüleneceğini belirtmek `ThisAddin` için projenizin sınıfındaki `CreateRibbonExtensibilityObject` yöntemi geçersiz kılın. Daha fazla bilgi için bkz. [Şerit 'e genel bakış](../vsto/ribbon-overview.md). Her şerit türü hakkında daha fazla bilgi için bkz. [Outlook 2007 'Deki şeridi özelleştirme](/previous-versions/office/developer/office-2007/bb226712(v=office.12))teknik makalesi.

## <a name="specify-the-ribbon-type-by-using-ribbon-xml"></a>Şerit XML kullanarak Şerit türünü belirtme
 **Şerit (XML)** öğesini kullanıyorsanız, <xref:Microsoft.Office.Core.IRibbonExtensibility.GetCustomUI%2A> yöntemindeki *ribbonID* parametresinin değerini kontrol edin ve uygun Şeriti döndürün.

 <xref:Microsoft.Office.Core.IRibbonExtensibility.GetCustomUI%2A> Yöntemi, Visual Studio tarafından Şerit kod dosyasında otomatik olarak oluşturulur. *RibbonID* parametresi, Gezgin 'i veya belirli bir Inspector türünü tanımlayan bir dizedir. *RibbonID* parametresinin olası değerlerinin tüm listesi için bkz. [Outlook 2007 'deki şeridi özelleştirme](/previous-versions/office/developer/office-2007/bb226712(v=office.12))teknik makalesi.

 Aşağıdaki kod örneği, özel bir şeridin yalnızca `Microsoft.Outlook.Mail.Compose` Inspector 'da nasıl görüntüleneceğini gösterir. Bu, Kullanıcı yeni bir e-posta iletisi oluşturduğunda açılan Inspector ' dır. Görüntülenecek Şerit, `GetResourceText()` **Şerit** sınıfında oluşturulan yönteminde belirtilir. **Şerit** sınıfı hakkında daha fazla bilgi için bkz. [Ribbon XML](../vsto/ribbon-xml.md).

 [!code-csharp[Trin_RibbonOutlookBasic#1](../vsto/codesnippet/CSharp/Trin_RibbonOutlookBasic/Ribbon1.cs#1)]
 [!code-vb[Trin_RibbonOutlookBasic#1](../vsto/codesnippet/VisualBasic/Trin_RibbonOutlookBasic/Ribbon1.vb#1)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma zamanında Şerite erişin](../vsto/accessing-the-ribbon-at-run-time.md)
- [Şerite Genel Bakış](../vsto/ribbon-overview.md)
- [Şerit Tasarımcısı](../vsto/ribbon-designer.md)
- [Şerit XML](../vsto/ribbon-xml.md)
