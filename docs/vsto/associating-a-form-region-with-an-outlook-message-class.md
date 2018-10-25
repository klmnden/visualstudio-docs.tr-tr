---
title: Form bölgesini Outlook ileti sınıfıyla ilişkilendirme
ms.custom: ''
ms.date: 02/02/2017
ms.technology: office-development
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- VSTO.NewFormRegionWizard.InvalidMessageClassName
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- FormRegionMessageClassAttribute
- form regions [Office development in Visual Studio], message classes
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 0a3b14086957d37809c8fbcba88386daff57be4a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49892005"
---
# <a name="associate-a-form-region-with-an-outlook-message-class"></a>Form bölgesini Outlook ileti sınıfıyla ilişkilendirme
  Form bölgesi her bir öğenin ileti sınıfıyla ilişkilendirme tarafından bir form bölgesi hangi Microsoft Office Outlook öğeleri görüntülemek belirtebilirsiniz. Örneğin, bir posta öğesinin altına bir form bölgesi eklemek istiyorsanız, form bölgesi ile ilişkilendirebilirsiniz `IPM.Note` ileti sınıfı.  
  
 Form bölgesini ileti sınıfıyla ilişkilendirme için ileti sınıf adını belirtin. **yeni Outlook Form bölgesi** Sihirbazı veya form bölgesi fabrikası sınıfına bir özniteliğini uygulayın.  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
## <a name="understand-outlook-message-classes"></a>Outlook ileti sınıflarını anlama  
 Outlook ileti sınıfı Outlook öğesi türünü tanımlar. Aşağıdaki tabloda bu sekiz standart türler öğeleri ve bunların ileti sınıf adları listelenmektedir.  
  
|Outlook öğesi türü|İleti sınıfı adı|  
|-----------------------|------------------------|  
|AppointmentItem|`IPM.Appointment`|  
|ContactItem|`IPM.Contact`|  
|DistListItem|`IPM.DistList`|  
|JournalItem|`IPM.Activity`|  
|MailItem|`IPM.Note`|  
|PostItem|`IPM.Post` veya `IPM.Post.RSS`|  
|TaskItem|`IPM.Task`|  
  
 Özel ileti sınıfların adlarını belirtebilirsiniz. Outlook'ta tanımladığınız özel formlar özel ileti sınıflarını tanımlayın.  
  
> [!NOTE]  
>  Değiştirme ve tümünü değiştirme form bölgeleri için yeni bir özel ileti sınıfı adı belirtebilirsiniz. Var olan bir özel formu ileti sınıfı adını kullanın gerekmez. Özel ileti sınıfı adı benzersiz olmalıdır. Adının benzersiz olduğundan emin olmanın bir yolu, aşağıdakine benzer bir adlandırma kuralı kullanmaktır: \< *StandardMessageClassName*>.\< *Şirket*>.\< *MessageClassName*> (örneğin: `IPM.Note.Contoso.MyMessageClass`).  
  
## <a name="associate-a-form-region-with-an-outlook-message-class"></a>Form bölgesini Outlook ileti sınıfıyla ilişkilendirme  
 Form bölgesini ileti sınıfıyla ilişkilendirme iki yolu vardır:  
  
-   Kullanım **yeni Outlook Form bölgesi** Sihirbazı.  
  
-   Sınıf öznitelikleri uygulanır.  
  
### <a name="use-the-new-outlook-form-region-wizard"></a>Yeni Outlook Form bölgesi sihirbazını kullanın  
 Son sayfasında **yeni Outlook Form bölgesi** sihirbazında, standart ileti sınıfları seçin ve form bölgesi ile ilişkilendirmek istediğiniz bir özel ileti sınıfları adlarını yazın.  
  
 Form bölgesini içerecek şekilde formun tamamını ya da formun varsayılan sayfasını değiştirmek üzere tasarlanmışsa, standart ileti sınıfları kullanılamaz. Bir forma yeni bir sayfa eklemek veya, form alt kısmına eklenir formları için standart ileti sınıf adları belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: bir Outlook eklenti projesine form bölgesi ekleme](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md).  
  
 Bir veya daha fazla özel ileti sınıflarını dahil etmek için adlarını yazın **hangi özel ileti sınıfları bu form bölgesini görüntüleyecek?** kutusu.  
  
 Yazdığınız ad, aşağıdaki yönergelere uymanız gerekir:  
  
- Tam ileti sınıfı adını kullanın (örneğin: "IPM. Note.Contoso").  
  
- Birden çok ileti sınıfı adını ayırmak için noktalı virgül kullanın.  
  
- "IPM. gibi standart Outlook ileti sınıflarını dahil etmeyin Not"veya"IPM. Başvurun". Yalnızca "IPM. gibi özel ileti sınıfları içerir. Note.Contoso".  
  
- Temel ileti sınıfını kendisi tarafından belirtmeyin (örneğin: "IPM").  
  
- Her ileti sınıfı adı 256 karakteri aşamaz.  
  
  **Yeni Outlook Form bölgesi** Sihirbazı tıkladığınızda giriş biçimini doğrular **son**.  
  
> [!NOTE]  
>  **Yeni Outlook Form bölgesi** Sihirbazı sağlayan ileti sınıf adları doğru ya da geçerli olduğunu doğrulamaz.  
  
 Sihirbazı tamamladığınızda **yeni Outlook Form bölgesi** sihirbaz, belirtilen ileti sınıfı adları içeren form bölgesi sınıfı öznitelikleri uygular. Bu öznitelikleri el ile de uygulayabilirsiniz.  
  
### <a name="apply-class-attributes"></a>Sınıf öznitelikleri uygulama  
 Tamamladıktan sonra form bölgesini Outlook ileti sınıfıyla ilişkilendirebilirsiniz **yeni Outlook Form bölgesi** Sihirbazı. Bunu yapmak için form bölgesi fabrikası sınıfına öznitelikleri uygulanır.  
  
 Aşağıdaki örnek iki gösterir <xref:Microsoft.Office.Tools.Outlook.FormRegionMessageClassAttribute> adlı form bölgesi fabrikası sınıfına uygulanan öznitelikleri `myFormRegion`. İlk öznitelik form bölgesini standart ileti sınıfı için bir posta iletisi form ile ilişkilendirir. İkinci öznitelik form bölgesinin adlı bir özel ileti sınıf ile ilişkilendirir `IPM.Task.Contoso`.  
  
 [!code-vb[Trin_Outlook_FR_Attributes#1](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Attributes/FormRegion1.vb#1)]
 [!code-csharp[Trin_Outlook_FR_Attributes#1](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Attributes/FormRegion1.cs#1)]  
  
 Öznitelik, aşağıdaki yönergelere uygun olmalıdır:  
  
- Özel ileti sınıfları için tam ileti sınıfı adını kullanın (örneğin: "IPM. Note.Contoso").  
  
- Temel ileti sınıfını kendisi tarafından belirtmeyin (örneğin: "IPM").  
  
- Her ileti sınıfı adı 256 karakteri aşamaz.  
  
- Form bölgesini içerecek şekilde formun tamamını veya bir formun varsayılan sayfasını değiştirir, standart ileti sınıflarının adları dahil değildir. Bir forma yeni bir sayfa eklemek veya, form alt kısmına eklenir formları için standart ileti sınıf adları belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: bir Outlook eklenti projesine form bölgesi ekleme](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md).  
  
  Proje oluşturduğunuzda, visual Studio ileti sınıf adları biçimini doğrular.  
  
> [!NOTE]  
>  Visual Studio sağlayan ileti sınıf adları doğru ya da geçerli olduğunu doğrulamaz.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Form bölgesine çalışma zamanında erişme](../vsto/accessing-a-form-region-at-run-time.md)   
 [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)   
 [İzlenecek yol: Outlook form bölgesi tasarlama](../vsto/walkthrough-designing-an-outlook-form-region.md)   
 [Outlook form bölgeleri oluşturma yönergeleri](../vsto/guidelines-for-creating-outlook-form-regions.md)   
 [Form adı ve ileti sınıfına genel bakış](http://msdn.microsoft.com/library/office/ff867629.aspx)   
 [Outlook form ve öğeleri birlikte nasıl çalışır](http://msdn.microsoft.com/library/office/ff869706.aspx)  
  
  