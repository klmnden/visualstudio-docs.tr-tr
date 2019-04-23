---
title: 'Nasıl yapılır: Bir iş akışı konsol uygulaması oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: 51a2eea7-921c-49f1-b358-68afc27f1ee9
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 33666c0e5d63d8d4d33d544fcfe18d8c185ce843
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60044358"
---
# <a name="how-to-create-a-workflow-console-application"></a>Nasıl yapılır: İş Akışı Konsol Uygulaması Oluşturma
[!INCLUDE[wf](../includes/wf-md.md)] Sistem ya da insan işlemleri yürütmek iş akışları oluşturmanıza olanak sağlar. [!INCLUDE[wfd1](../includes/wfd1-md.md)] Bu iş akışları oluşturmak için tasarım yüzeyi sağlar. [!INCLUDE[wfd2](../includes/wfd2-md.md)] İçinden iş akışları oluşturmak için kullanılan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] veya tasarımcıyı yeniden barındırma diğer uygulamalarda tümleştirilebilir.  
  
 Bu konu nasıl kullanılacağını açıklar [!INCLUDE[wfd2](../includes/wfd2-md.md)] içinde [!INCLUDE[vs2010](../includes/vs2010-md.md)] bir konsol uygulamasında bir iş akışı oluşturmak için.  
  
### <a name="to-create-a-workflow-console-application"></a>Bir iş akışı konsol uygulaması oluşturmak için  
  
1. Başlangıç [!INCLUDE[vs2010](../includes/vs2010-md.md)].  
  
2. Üzerinde **dosya** menüsünde **yeni**ve ardından **proje...** .  
  
     **Yeni proje** iletişim kutusu açılır.  
  
3. İçinde **yüklü şablonlar** bölmesinde **iş akışı** da **Visual C#** veya **Visual Basic** gruplandırmaları, bağlı olarak, dil tercihi.  
  
4. Orta bölmede seçin **iş akışı konsol uygulaması**.  
  
5. İçinde **adı** kutusunda, tanımlamakta kolaylaştırmak, projeniz için açıklayıcı bir ad girin.  
  
6. İçinde **konumu** kutusunda, projeyi kaydedin veya istediğiniz dizin girin **Gözat** gitmek için.  
  
7. İçinde **çözüm** kutusunda, yeni çözüm için bir ad girin. Tıklayın **Tamam** uygulama oluşturmak için.  
  
    > [!NOTE]
    >  Varolan bir çözüm için bir iş akışı konsol uygulaması eklemek istiyorsanız, bu çözümde açık [!INCLUDE[vs2010](../includes/vs2010-md.md)], çözüme sağ tıklayın **Çözüm Gezgini**seçip **Ekle**, ardından  **Yeni proje...** açmak için **yeni proje** iletişim kutusu. Bu yordamda yukarıda açıklanan şekilde devam edin.  
  
8. Proje şablonu, XAML içinde bir iş akışı tanımı oluşturur ve kaynak kodunda konsol uygulamanın tanımıdır. [!INCLUDE[wfd2](../includes/wfd2-md.md)] Açılır ve oluşturduğunuz iş akışı için tuvalde görüntüler.  
  
9. Bir iş akışı oluşturmak için etkinlikler veya diğer iş akışı öğeleri sürükleyin **araç kutusu** akışınızın tasarım yüzeyine.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Akışı Projesi Oluşturma](../workflow-designer/creating-a-workflow-project.md)