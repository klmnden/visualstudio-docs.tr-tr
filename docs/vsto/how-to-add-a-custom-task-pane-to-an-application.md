---
title: 'Nasıl yapılır: Uygulamaya özel görev bölmesi ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- task panes [Office development in Visual Studio], adding to application
- custom task panes [Office development in Visual Studio], adding to application
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 047728f00fae9dbf3cf2511300beaa84c2201cdd
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60039849"
---
# <a name="how-to-add-a-custom-task-pane-to-an-application"></a>Nasıl yapılır: Uygulamaya özel görev bölmesi ekleme
  VSTO eklentisi kullanarak bir özel görev bölmesi uygulamaları için yukarıda listelenen ekleyebilirsiniz. Daha fazla bilgi için [özel görev bölmeleri](../vsto/custom-task-panes.md).

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

> [!NOTE]
>  Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md).

## <a name="add-a-custom-task-pane-to-an-application"></a>Uygulamaya özel görev bölmesi ekleme

### <a name="to-add-a-custom-task-pane-to-an-application"></a>Uygulamaya özel görev bölmesi ekleme

1. Bir VSTO eklentisi projesi için yukarıda listelenen uygulamalardan birini oluşturun veya açın. Daha fazla bilgi için [nasıl yapılır: Visual Studio'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md).

2. Üzerinde **proje** menüsünü tıklatın **kullanıcı denetimi Ekle**.

3. İçinde **Yeni Öğe Ekle** iletişim kutusunda, yeni kullanıcı denetimine adını değiştirmek **MyUserControl**ve ardından **Ekle**.

     Kullanıcı denetimi Tasarımcısı'nda açılır.

4. Bir veya daha fazla Windows Forms denetimleri ekleme **araç kutusu** kullanıcı denetimi için.

5. Açık **ThisAddIn.cs** veya **ThisAddIn.vb** kod dosyası.

6. Aşağıdaki kodu ekleyin `ThisAddIn` sınıfı. Bu kod örneğini bildirir `MyUserControl` ve <xref:Microsoft.Office.Tools.CustomTaskPane> üyesi olarak `ThisAddIn` sınıfı.

     [!code-vb[Trin_TaskPaneBasic#1](../vsto/codesnippet/VisualBasic/Trin_TaskPaneBasic/ThisAddIn.vb#1)]
     [!code-csharp[Trin_TaskPaneBasic#1](../vsto/codesnippet/CSharp/Trin_TaskPaneBasic/ThisAddIn.cs#1)]

7. Aşağıdaki kodu ekleyin `ThisAddIn_Startup` olay işleyicisi. Bu kod yeni bir oluşturur <xref:Microsoft.Office.Tools.CustomTaskPane> ekleyerek `MyUserControl` nesnesini `CustomTaskPanes` koleksiyonu. Kod ayrıca görev bölmesini görüntüler.

     [!code-vb[Trin_TaskPaneBasic#2](../vsto/codesnippet/VisualBasic/Trin_TaskPaneBasic/ThisAddIn.vb#2)]
     [!code-csharp[Trin_TaskPaneBasic#2](../vsto/codesnippet/CSharp/Trin_TaskPaneBasic/ThisAddIn.cs#2)]

    > [!NOTE]
    >  Bu kod, özel görev bölmesi uygulamasında etkin pencere ilişkilendirir. Bazı uygulamalar için görev bölmesinde diğer belgelerin veya öğelerin uygulamada göründüğüne emin olmak için bu kodu değiştirmek isteyebilirsiniz. Daha fazla bilgi için [özel görev bölmeleri](../vsto/custom-task-panes.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office kullanıcı arabirimini özelleştirme](../vsto/office-ui-customization.md)
- [Özel görev bölmeleri](../vsto/custom-task-panes.md)
- [İzlenecek yol: Bir uygulamayı özel görev bölmesinden otomatikleştirme](../vsto/walkthrough-automating-an-application-from-a-custom-task-pane.md)
