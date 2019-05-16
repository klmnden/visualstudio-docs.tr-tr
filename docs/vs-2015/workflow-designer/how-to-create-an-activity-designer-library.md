---
title: 'Nasıl yapılır: Bir etkinlik Tasarımcısı kitaplığı oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: 5b62e092-63b3-462d-9d77-fb112482f45d
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a51b4cdb67590b908bc406b78c04ddf0c5aa3e2f
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694553"
---
# <a name="how-to-create-an-activity-designer-library"></a>Nasıl yapılır: Etkinlik Tasarımcısı Kitaplığı Oluşturma
Özel Etkinlik tasarımcıları bir standart veya özel bir etkinlik için bir kullanıcı arabirimi oluşturmanıza imkan tanır. Artık kullanıcı arabiriminin karmaşıklığı denetlemek ve bir etkinliğin birden fazla etkinlik Tasarımcısı oluşturma olanağı. Bu senaryo için birden çok İzleyici uyarlandığından tasarımcıları oluşturmanıza olanak sağlar.  
  
### <a name="to-create-an-activity-designer-library"></a>Bir etkinlik Tasarımcısı kitaplığı oluşturmak için  
  
1. Başlangıç [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2. Üzerinde **dosya** menüsünde **yeni**ve ardından **proje...** açmak için **yeni proje** iletişim kutusu.  
  
3. İçinde **proje türleri** bölmesinde **iş akışı** da **Visual C#** veya **Visual Basic** gruplandırmaları bağlı olarak tercih ettiğiniz dili.  
  
4. İçinde **şablonları** bölmesinde **etkinlik Tasarımcısı Kitaplığı**.  
  
5. İçinde **adı** kutusunda, tanımlamakta kolaylaştırmak, projeniz için açıklayıcı bir ad girin.  
  
6. İçinde **konumu** kutusunda, projeyi kaydedin veya istediğiniz dizin girin **Gözat** gitmek için.  
  
7. İçinde **çözüm** kutusunda, çözümünüz için açıklayıcı bir ad yazın ve ardından tıklayın **Tamam**.  
  
    > [!NOTE]
    > Varolan bir çözüm için bir iş akışı konsol uygulaması eklemek istiyorsanız, bu çözümde açık [!INCLUDE[vs2010](../includes/vs2010-md.md)], çözüme sağ tıklayın **Çözüm Gezgini**seçip **Ekle**, ardından **Yeni proje...** açmak için **yeni proje** iletişim kutusu. Bu yordamda yukarıda açıklanan şekilde devam edin.  
  
8. Proje şablonu, XAML ve arka plan kod uygulama kaynak kodu dosyasında bir etkinlik tasarımcısının tanımı oluşturur. [!INCLUDE[wfd1](../includes/wfd1-md.md)] Açılır ve tuval, etkinlik Tasarımcısı için görüntüler.  
  
9. Sürükleme [!INCLUDE[avalon1](../includes/avalon1-md.md)] denetimler **araç kutusu** özel etkinlik Tasarımcısı'nda kullanılacak tasarım yüzeyine bırakın.  Özel Etkinlik Tasarımcısı uygulamak nasıl bir örnek için bkz [nasıl yapılır: Özel Etkinlik Tasarımcısı oluşturma](https://msdn.microsoft.com/library/2f3aade6-facc-44ef-9657-a407ef8b9b31).  
  
    > [!WARNING]
    > Özel Etkinlik tasarımcıları, varsayılan hem de özel etkinlikler için kullanılabilir [!INCLUDE[netfx40_short](../includes/netfx40-short-md.md)]etkinlikler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Akışı Projesi Oluşturma](../workflow-designer/creating-a-workflow-project.md)