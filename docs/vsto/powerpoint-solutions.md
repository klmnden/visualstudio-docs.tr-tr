---
title: PowerPoint çözümleri
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office solutions [Office development in Visual Studio], PowerPoint
- templates [Office development in Visual Studio], PowerPoint
- solutions [Office development in Visual Studio], PowerPoint
- projects [Office development in Visual Studio], PowerPoint
- PowerPoint [Office development in Visual Studio]
- Office projects [Office development in Visual Studio], PowerPoint
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 9d2c85a4af986c62d3e3f3c3a3f4333baa2975ee
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926428"
---
# <a name="powerpoint-solutions"></a>PowerPoint çözümleri
  Visual Studio, Microsoft Office PowerPoint için VSTO eklentileri oluşturmak için kullanabileceğiniz proje şablonları sağlar. PowerPoint 'i otomatikleştirebilmek, PowerPoint özelliklerini genişletmek veya PowerPoint Kullanıcı arabirimini (UI) özelleştirmek için VSTO Eklentilerini kullanabilirsiniz.

 VSTO eklentileri hakkında daha fazla bilgi için bkz. VSTO eklentileri ve VSTO eklentilerinin [mimarisi](../vsto/architecture-of-vsto-add-ins.md) [programlamasına](../vsto/getting-started-programming-vsto-add-ins.md) başlama. Microsoft Office ile programlama konusunda yeni başladıysanız bkz. [Visual Studio&#41;'da &#40;çalışmaya başlama Office geliştirme](../vsto/getting-started-office-development-in-visual-studio.md).

 [!INCLUDE[appliesto_pptallapp](../vsto/includes/appliesto-pptallapp-md.md)]

> [!NOTE]
> Office deneyiminiz boyunca genişleten çözümleri geliştirme yapmakla mı ilgileniyorsunuz [birden çok platform](https://dev.office.com/add-in-availability)? Yeni kontrol [Office eklentilerini modeli](https://dev.office.com/docs/add-ins/overview/office-add-ins). Office eklentileri, VSTO eklentileri ve çözümlerle karşılaştırıldığında küçük ayak izine sahip ve neredeyse tüm web teknolojisi, HTML5, JavaScript, CSS3 ve XML gibi programlama kullanarak oluşturabilirsiniz.

 ![video bağlantısı](../vsto/media/playvideo.gif "video bağlantısı") İlgili video gösterimi için bkz [. nasıl yaparım?: Microsoft PowerPoint için bir eklenti oluşturulsun mu? ](http://go.microsoft.com/fwlink/?LinkId=132767).

## <a name="automate-powerpoint-by-using-the-powerpoint-object-model"></a>PowerPoint nesne modelini kullanarak PowerPoint 'i otomatikleştirin
 PowerPoint nesne modeli, PowerPoint 'i otomatikleştirmek için kullanabileceğiniz birçok türü kullanıma sunar. Bu türler ortak görevleri gerçekleştirmek için kod yazmanıza olanak sağlar:

- Program aracılığıyla sunular oluşturun ve biçimlendirin.

- Sunumlardan slaytlar ekleyin veya kaldırın.

- Slaytlara şekil ekleme veya şekilleri değiştirme.

  Bir VSTO eklentisinin PowerPoint nesne modeline erişmek için, projenizdeki `Application` `ThisAddIn` sınıfının alanını kullanın. Alan `Application` , PowerPoint 'in geçerli örneğini temsil eden bir [uygulama](/previous-versions/office/developer/office-2010/ff764034(v=office.14)) nesnesi döndürür. Daha fazla bilgi için bkz. [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md).

  PowerPoint nesne modeli ' ne çağırdığınızda, PowerPoint için birincil birlikte çalışma derlemesinde sunulan türleri kullanırsınız. Birincil birlikte çalışma derlemesi, VSTO eklentisinin yönetilen kodu ile PowerPoint 'teki COM nesne modelinde bir köprü görevi görür. PowerPoint birincil birlikte çalışma derlemesindeki tüm türler, [Microsoft. Office. Interop. PowerPoint](/previous-versions/office/developer/office-2010/ff763170(v=office.14)) ad alanında tanımlanmıştır. Birincil birlikte çalışma derlemeleri hakkında daha fazla bilgi için bkz. [Office çözümleri &#40;geliştirmeye&#41; genel bakış VSTO](../vsto/office-solutions-development-overview-vsto.md) ve [Office birincil birlikte çalışma derlemeleri](../vsto/office-primary-interop-assemblies.md).

## <a name="WordOMDocumentation"></a>PowerPoint nesne modeli belgelerini kullanma
 PowerPoint nesne modeli hakkında tüm bilgiler için, PowerPoint birincil birlikte çalışma derlemesi (PIA) başvurusuna ve VBA nesne modeli başvurusuna başvurabilirsiniz.

### <a name="primary-interop-assembly-reference"></a>Birincil birlikte çalışma derleme başvurusu
 PowerPoint PIA başvuru belgeleri, PowerPoint için birincil birlikte çalışma derlemesindeki türleri açıklar. Bu belge aşağıdaki konumdan edinilebilir: [PowerPoint 2010 birincil birlikte çalışma derleme başvurusu](http://go.microsoft.com/fwlink/?LinkId=189588).

 PIA içindeki sınıflar ve arabirimler arasındaki farklar ve PIA 'teki olayların nasıl uygulandığı gibi, PowerPoint PIA tasarımı hakkında daha fazla bilgi için bkz. [Office birincil birlikte çalışma derlemelerindeki sınıflara ve arabirimlere genel bakış](http://go.microsoft.com/fwlink/?LinkId=199885).

### <a name="vba-object-model-reference"></a>VBA nesne modeli başvurusu
 VBA nesne modeli başvurusu, Visual Basic for Applications (VBA) koduna açık olduğu için PowerPoint nesne modelini belgeler. Daha fazla bilgi için bkz. [PowerPoint 2010 nesne modeli başvurusu](http://go.microsoft.com/fwlink/?LinkId=199770).

 VBA nesne modeli başvurusundaki tüm nesneler ve Üyeler, PowerPoint birincil birlikte çalışma derlemesindeki (PIA) türlere ve üyelere karşılık gelir. Örneğin, VBA nesne modeli başvurusundaki sunum nesnesi, PowerPoint PIA içindeki [sunum](/previous-versions/office/developer/office-2010/ff761925(v=office.14)) türüne karşılık gelir. VBA nesne modeli başvurusu birçok özellik, yöntem ve olay için kod örnekleri sağlasa da, bunları tarafından oluşturduğunuz bir PowerPoint VSTO eklentisi projesinde kullanmak istiyorsanız bu başvurudaki VBA kodunu Visual Basic C# veya görsele çevirmeniz gerekir Visual Studio 'Yu kullanma.

## <a name="customize-the-user-interface-of-powerpoint"></a>PowerPoint 'in Kullanıcı arabirimini özelleştirme
 PowerPoint Kullanıcı arabirimini aşağıdaki yollarla değiştirebilirsiniz.

|Görev|Daha fazla bilgi için|
|----------|--------------------------|
|Özel görev bölmesi oluşturun.|[Özel görev bölmeleri](../vsto/custom-task-panes.md)|
|Şerite özel sekmeler ekleyin.|[Şerite Genel Bakış](../vsto/ribbon-overview.md)|
|Şeritteki yerleşik bir sekmeye özel gruplar ekleyin.|[Nasıl yapılır: Yerleşik bir sekmeyi özelleştirme](../vsto/how-to-customize-a-built-in-tab.md)|

 PowerPoint ve diğer Microsoft Office uygulamalarının Kullanıcı arabirimini özelleştirme hakkında daha fazla bilgi için bkz. [OFFICE UI özelleştirmesi](../vsto/office-ui-customization.md).

## <a name="see-also"></a>Ayrıca bkz.
- [İzlenecek yol: PowerPoint için ilk VSTO eklentisini oluşturma](../vsto/walkthrough-creating-your-first-vsto-add-in-for-powerpoint.md)
- [VSTO Eklentilerini Programlamaya Başlama](../vsto/getting-started-programming-vsto-add-ins.md)
- [Office çözümleri geliştirmesine genel &#40;bakış VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md)
- [VSTO Eklentileri Mimarisi](../vsto/architecture-of-vsto-add-ins.md)
- [Nasıl yapılır: Visual Studio 'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)
- [Office birincil birlikte çalışma derlemeleri](../vsto/office-primary-interop-assemblies.md)
- [Office UI özelleştirmesi](../vsto/office-ui-customization.md)
- [Office geliştirme 'da PowerPoint 2010](http://go.microsoft.com/fwlink/?LinkId=199015)
