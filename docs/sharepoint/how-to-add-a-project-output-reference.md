---
title: 'Nasıl yapılır: Proje çıktı başvurusu ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- project output references [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, project output references
- SharePoint development in Visual Studio, advanced packaging tools
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2ae3965647416d7a8e11cf0ea5e24cef1e54a09b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60079791"
---
# <a name="how-to-add-a-project-output-reference"></a>Nasıl yapılır: Proje çıktı başvurusu ekleme
  SharePoint Proje derlemeleri (veya Silverlight projelerinde .xap dosyaları) için SharePoint dağıtmak için proje çıktı başvurusu ekleyin.

 Bu işlem, iki proje arasında bir çözüm derleme bağımlılığı oluşturur. SharePoint Proje oluşturulan ve dağıtılan önce proje çıktı başvuruları ile ilişkili projeler oluşturulur.

### <a name="to-add-a-project-output-reference"></a>Proje çıktı başvurusu ekleme

1. En az bir SharePoint projesi ve bir SharePoint olmayan proje içeren bir çözüm yükleyin.

2. İçinde **Çözüm Gezgini**, SharePoint proje düğümünde bir öğeyi seçin.

3. İçinde **özellikleri** penceresinde seçin **proje çıktı başvuruları** özelliği ve ardından üç noktayı seçin (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP. NET Mobil Tasarımcısı elips")) yanında düğmesi.

4. İçinde **proje çıktı başvuruları** iletişim kutusunda **Ekle** düğmesi.

5. Özellikler bölmesinde yanındaki oku seçin **dağıtım türü** özelliği başvuruda, gibi SharePoint öğe için uygun değeri seçin **ElementFile**.

6. Yanındaki oku seçin **proje adı**olmayan SharePoint proje öğesi adını seçin ve ardından **Tamam** düğmesi.

## <a name="see-also"></a>Ayrıca bkz.
- [Proje öğelerinde paketleme ve dağıtım bilgileri sağlayın](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)
- [Nasıl yapılır: Denetimleri güvenli denetim olarak işaretleme](../sharepoint/how-to-mark-controls-as-safe-controls.md)
- [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
