---
title: 'Nasıl yapılır: Bir Outlook eklenti projesine form bölgesi ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VSTO.NewFormRegionWizard.Page1
- VSTO.NewFormRegionWizard.Page3
- VSTO.NewFormRegionWizard.Page2
- VSTO.NewFormRegionWizard.Page0
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- form regions [Office development in Visual Studio], adding
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5c742b4cbbda440ea84314efbc5281e54771fe60
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63427887"
---
# <a name="how-to-add-a-form-region-to-an-outlook-add-in-project"></a>Nasıl yapılır: Bir Outlook eklenti projesine form bölgesi ekleme
  Bir standart veya özel Microsoft Office Outlook biçimini kullanarak genişletmek için bir form bölgesi oluşturabilir **yeni Outlook Form bölgesi** Sihirbazı. Yeni bir form bölgesi oluşturabilir ve Visual Studio kullanıcı arabiriminde tasarım ya da Outlook'ta tasarlanan form bölgesini içeri aktarabilir ve Visual Basic ekleyin veya C# kod.

 Başka bir Outlook projesinde kullanılan Outlook form bölgesi varsa, onu geçerli Outlook VSTO eklenti projenizde kullanarak tekrar kullanabilirsiniz **varolan öğeyi Ekle** iletişim kutusu. Daha fazla bilgi için [oluşturma Outlook form bölgeleri](../vsto/creating-outlook-form-regions.md).

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

### <a name="to-add-a-new-form-region-to-an-outlook-project"></a>Yeni form bölgesini Outlook projesine eklemek için

1. Bir Outlook VSTO eklentisi projesi oluşturun veya açın [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Daha fazla bilgi için [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md).

2. İçinde **Çözüm Gezgini**, Outlook VSTO eklentisi proje düğümünü seçin.

3. Üzerinde **proje** menüsünü tıklatın **Yeni Öğe Ekle**.

4. İçinde **Yeni Öğe Ekle** iletişim kutusunda **Outlook Form bölgesi**.

5. Form bölgesinin için bir ad yazın **adı** kutusuna ve ardından **Ekle**.

     **NewOutlook Form bölgesi** Sihirbazı'nı başlatır.

6. Üzerinde **nasıl form bölgesi oluşturmak istediğinizi seçin** sayfasında, yönetilen denetimleri bir görsel tasarımcıya sürükleyerek form bölgesi tasarla ya da Outlook'ta tasarlanan form bölgesini almak isteyip istemediğinizi seçin.

    > [!NOTE]
    > Outlook'ta tasarlanan form bölgesini içeri aktarmak seçtiğiniz ardından Outlook Form depolama konumu belirtmeniz gerekir (*.ofs*) dosyası. Form bölgesini Outlook tasarım yönetilen denetimleri eklenemiyor; yalnızca var olan kullanıcı arabirimini arka plan kod ekleyebilirsiniz. Daha fazla bilgi için [oluşturma Outlook form bölgeleri](../vsto/creating-outlook-form-regions.md).

7. Üzerinde **oluşturmak istediğiniz form bölgesi türünü seçin** sayfasında form bölgesi türleri gözden geçirin ve seçin ve ardından **sonraki**. Form bölgesi türleri hakkında daha fazla bilgi için bkz. [oluşturma Outlook form bölgeleri](../vsto/creating-outlook-form-regions.md).

8. Üzerinde **açıklayıcı metni sağlayın ve görüntüleme tercihlerinizi seçin** sayfasında **adı** form bölgesi için bir ad yazın. Değiştirme ve tümünü değiştirme form bölgesi türleri **başlık** ve **açıklama** kutuları de mevcuttur.

     Form bölgesinin dağıttığınızda, ad, başlık ve açıklama Outlook'ta nerede görüneceğini hakkında daha fazla bilgi için bkz: [oluşturma Outlook form bölgeleri](../vsto/creating-outlook-form-regions.md).

9. Form bölgesinin görünmesini istediğiniz bir veya daha fazla görüntü modları seçin.

     Tüm form bölgesi türleri Inspector, görünebilir içinde modu (için öğeleri oluşturma) oluşturun ve (öğeleri görüntüleme için) okuma modunda. Bitişik, değiştirme ve tümünü değiştirme form bölgesi türleri de Okuma Bölmesi'nde görünür.

10. **İleri**'ye tıklayın.

11. Üzerinde **bu form bölgesini görüntüleyecek ileti sınıflarını tanımlayın** sayfasında standart Outlook ileti sınıflarını seçin veya bir veya daha fazla özel ileti sınıf adlarını yazın ve ardından **son**. Daha fazla bilgi için [form bölgesini Outlook ileti sınıfıyla ilişkilendirme](../vsto/associating-a-form-region-with-an-outlook-message-class.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Form bölgesine çalışma zamanında erişme](../vsto/accessing-a-form-region-at-run-time.md)
- [Outlook çözümleri](../vsto/outlook-solutions.md)
- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)
- [Yönergeler için Outlook form bölgeleri oluşturma](../vsto/guidelines-for-creating-outlook-form-regions.md)
- [İzlenecek yol: Outlook form bölgesi tasarlama](../vsto/walkthrough-designing-an-outlook-form-region.md)
- [İzlenecek yol: Outlook'ta tasarlanan form bölgesini içeri aktarma](../vsto/walkthrough-importing-a-form-region-that-is-designed-in-outlook.md)
- [Outlook form bölgelerindeki özel eylemler](../vsto/custom-actions-in-outlook-form-regions.md)
