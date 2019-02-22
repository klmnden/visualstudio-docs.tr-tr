---
title: 'Nasıl yapılır: Bir SharePoint Web Bölümü oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Web Parts [SharePoint development in Visual Studio], adding
- Web Parts [SharePoint development in Visual Studio], creating
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3328c8900a202dd28eb2cab7c9651de8f45aa35e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56636924"
---
# <a name="how-to-create-a-sharepoint-web-part"></a>Nasıl yapılır: Bir SharePoint web bölümü oluşturma
  Oluşturma ve bir web bölümü ekleyerek özelleştirin bir **Web Bölümü** öğesi herhangi bir SharePoint projesine ve ardından bir Tasarımcısını kullanarak veya web bölümü için kod dosyasını düzenleme. Daha fazla bilgi için [nasıl yapılır: Tasarımcı kullanarak bir SharePoint web bölümü oluşturma](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md).

### <a name="to-create-a-sharepoint-web-part"></a>Bir SharePoint web bölümü oluşturmak için

1.  Oluşturun veya bir SharePoint projesi açın.

     Daha fazla bilgi için [SharePoint projesi ve proje öğesi şablonları](../sharepoint/sharepoint-project-and-project-item-templates.md).

2.  SharePoint proje düğümünde seçin **Çözüm Gezgini** seçip **proje** > **Yeni Öğe Ekle**.

3.  İçinde **Yeni Öğe Ekle** iletişim kutusunda **SharePoint** düğümünü seçip **2010** düğümü.

4.  SharePoint şablonları listesinde seçin **Web Bölümü**.

5.  İçinde **adı** kutusunda, web bölümü için bir ad belirtin ve ardından **Ekle** düğmesi.

     Web bölümü görünür **Çözüm Gezgini**. Bir web bölümü içeren dosyalar hakkında daha fazla bilgi için bkz. [için SharePoint web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md).

6.  İçinde **Çözüm Gezgini**, yeni oluşturduğunuz web bölümü için kod dosyasını açın.

     Örneğin, web bölümünün adı ise *WebPart1*açın *WebPart1.vb* (Visual Basic'te) veya *WebPart1.cs* (içinde C#).

7.  Kod dosyasında, ekleme denetimlerini <xref:System.Web.UI.Control.CreateChildControls%2A> yöntemi.

     Bir örnek için bkz [izlenecek yol: SharePoint için bir web bölümü oluşturma](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)
- [Nasıl yapılır: Tasarımcı kullanarak bir SharePoint web bölümü oluşturma](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md)
- [İzlenecek yol: SharePoint için bir web bölümü oluşturma](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md)
- [İzlenecek yol: Tasarımcı kullanarak SharePoint için bir web bölümü oluşturma](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint-by-using-a-designer.md)
