---
title: 'Nasıl yapılır: Eklenti kullanıcı arayüzü hatalarını gösterme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- add-ins [Office development in Visual Studio], user interface errors
- errors [Office development in Visual Studio], user interface errors
- user interfaces [Office development in Visual Studio], errors
- application-level add-ins [Office development in Visual Studio], user interface errors
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 34727c0949ab4ad6baf8e91b27b20115cf074b92
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60096367"
---
# <a name="how-to-show-add-in-user-interface-errors"></a>Nasıl yapılır: Eklenti kullanıcı arayüzü hatalarını gösterme
  Microsoft Office kullanıcı arabirimini (UI) ve başarısız olursa, işlemek VSTO eklentisi eşleşmeye çalışıyorsa, varsayılan olarak, hata iletisi görüntülenir. Ancak, Microsoft Office uygulamaları için kullanıcı Arabirimi ile ilgili hata iletileri görüntülemek için yapılandırabilirsiniz. Bu iletiler, özel bir Şerit bulunmamasının veya neden bir Şerit görünür ancak denetim yok görünür belirlemeye yardımcı olması için kullanabilirsiniz.

 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]

## <a name="to-show-vsto-add-in-user-interface-errors"></a>VSTO eklenti kullanıcı arayüzü hatalarını göstermek için

1. Uygulamayı başlatın.

2. Tıklayın **dosya** sekmesi.

3. Tıklayın **seçenekleri**.

4. Kategorileri bölmesinden **Gelişmiş**.

5. Ayrıntılar bölmesinde seçin **kullanıcı arayüzü hatalarını gösterme VSTO eklentisi**ve ardından **Tamam**.

    > [!NOTE]
    >  Outlook için **kullanıcı arayüzü hatalarını gösterme VSTO eklentisi** onay kutusu bulunan **Geliştirici** Ayrıntılar bölümünde. Diğer uygulamalar için onay kutusunu bulunan **genel** Ayrıntılar bölümünde.

## <a name="see-also"></a>Ayrıca bkz.
- [Office kullanıcı arabirimini özelleştirme](../vsto/office-ui-customization.md)
- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)
- [Şerite Genel Bakış](../vsto/ribbon-overview.md)
- [Eylemler bölmesine genel bakış](../vsto/actions-pane-overview.md)
