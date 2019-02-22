---
title: Web Bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- user controls [SharePoint development in Visual Studio], creating
- SharePoint development in Visual Studio, user controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 71e67ab41fd39563520370eb079fca1b7c82015e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56601141"
---
# <a name="create-reusable-controls-for-web-parts-or-application-pages"></a>Web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma
  Visual Studio'da Uygulama sayfaları ve SharePoint'te çalışan Web bölümleri tarafından kullanılabilen özel, yeniden kullanılabilir denetimler oluşturabilirsiniz. Bu denetimler, kullanıcı denetimleri olarak adlandırılır. Bir kullanıcı denetimi, çalışan bir ASP.NET Web sayfası gibi bileşik denetim türüdür; bir kullanıcı denetimine mevcut Web sunucusu denetimleri ve biçimlendirme ekleme ve denetim için özellikleri ve yöntemleri tanımlar. Daha sonra bunları nerede bunlar bir birim olarak davranan, ASP.NET Web sayfalarında katıştırabilirsiniz.

## <a name="create-a-user-control"></a>Bir kullanıcı denetimi oluşturma
 Bir kullanıcı denetimi oluşturmak için bir **kullanıcı denetimi** için bir **boş SharePoint projesi**. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint uygulama sayfası veya web bölümü için bir kullanıcı denetimi oluşturma](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md).

 Eklediğinizde bir **kullanıcı denetimi** öğesi, Visual Studio projenize bir klasör oluşturur ve ardından çeşitli dosyalar klasörüne ekler. Aşağıdaki tabloda her dosya açıklanmaktadır.

|Dosya|Açıklama|
|----------|-----------------|
|Kullanıcı denetimi dosyası|Kullanıcı denetimini tanımlar. Kullanıcı denetimi, denetimleri ve biçimlendirme, bu dosyaya ekleyerek tasarlayın.|
|Kod dosyası|Kullanıcı denetiminin arka plan kod içerir. Bu dosyaya olaylarını işlemek için kod ekleyin.|
|Tasarımcı kod dosyası|Tasarımcı tarafından oluşturulan kodu içerir ve be doğrudan düzenlenemez.|

## <a name="design-the-user-control"></a>Kullanıcı denetimi tasarlama
 Visual Studio'da Visual Web Developer Tasarımcısını kullanarak kullanıcı denetiminin tasarım. Bu tasarımcı, projenizde kullanıcı denetimini dosyasını açın ve seçtiğinizde görünür **tasarım** sekmesi.

## <a name="consume-the-user-control"></a>Kullanıcı denetimi kullanma
 Kullanıcı denetimleri, bunları bir uygulama sayfası veya bir Web Bölümü eklemek kadar SharePoint'te görünmez.

 Uygulama sayfası bir kullanıcı denetimi eklemek için ASP.NET kullanıcı denetimi eklemek istediğiniz Web sayfasını açın. Tasarım görünümüne sonra özel kullanıcı denetimi dosyanızın Çözüm Gezgini'nde seçin ve sayfanın üzerine sürükleyin. ASP.NET kullanıcı denetimi sayfasına eklenir ve tasarımcı sayfası kullanıcı Denetimi'ni tanımak üzere gerekli olan @ Register yönergesi oluşturur. Artık, denetimin ortak özelliklerini ve yöntemlerini ile çalışabilirsiniz.

 Bir kullanıcı denetimi içinde bir Web Bölümü eklemek için Web Bölümü için kullanıcı denetimi Ekle <xref:System.Web.UI.WebControls.WebParts.Part.Controls%2A> Web Bölümü kod dosyasında koleksiyonu. Aşağıdaki örnek, bir kullanıcı denetimine ekler <xref:System.Web.UI.WebControls.WebParts.Part.Controls%2A> bir Web Bölümü koleksiyonu.

 [!code-vb[SP_VisualWebPart#5](../sharepoint/codesnippet/VisualBasic/sp_visualwebpart.vb/visualwebpart1/visualwebpart1.vb#5)]
 [!code-csharp[SP_VisualWebPart#5](../sharepoint/codesnippet/CSharp/sp_visualwebpart.cs/visualwebpart1/visualwebpart1.cs#5)]

## <a name="debug-a-user-control"></a>Bir kullanıcı denetiminde hata ayıklama
 Bir kullanıcı denetimi hata ayıklamak için kullanıcı denetiminin bir uygulama sayfası veya Web Bölümü SharePoint projenizde yer aldığından emin olun. Tüm Visual Studio proje kodu hatalarını ayıklama gibi kullanıcı denetiminde kod sonra hata ayıklaması yapabilirsiniz.

 Visual Studio hata ayıklayıcısını başlattığınızda, Visual Studio SharePoint sitesi açılır.

 SharePoint'te, kullanıcı denetimi içeren uygulamanın sayfasını açın. Kullanıcı denetimi içinde bir Web Bölümü eklediyseniz, Web Bölümünü bir SharePoint Web Bölümü sayfasına ekleyin.

 SharePoint projelerinde hata ayıklama hakkında daha fazla bilgi için bkz. [sorun giderme SharePoint çözümleri](../sharepoint/troubleshooting-sharepoint-solutions.md).

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[Nasıl yapılır: Bir SharePoint uygulama sayfası veya web bölümü için bir kullanıcı denetimi oluşturma](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md)|Uygulama sayfaları ve SharePoint'te çalışan Web bölümleri tarafından kullanılabilen özel, yeniden kullanılabilir denetimler oluşturma işlemi gösterilmektedir.|
