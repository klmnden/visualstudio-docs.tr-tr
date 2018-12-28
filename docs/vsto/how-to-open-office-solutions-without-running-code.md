---
title: 'Nasıl Yapılır: Kod çalıştırmadan Office çözümlerini açma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office solutions [Office development in Visual Studio], opening
- opening Office solutions
- bypassing assemblies
- solutions [Office development in Visual Studio], opening
- assemblies [Office development in Visual Studio], bypassing
- Office documents [Office development in Visual Studio, opening without running code
- documents [Office development in Visual Studio], opening without running code
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 7684fd2d01d0151798c9e59c593e3e0c2acb95b1
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53646912"
---
# <a name="how-to-open-office-solutions-without-running-code"></a>Nasıl Yapılır: Kod çalıştırmadan Office çözümlerini açma
  Yönetilen kod uzantıları ile oluşturulan Microsoft Office çözümü son kullanıcı Office uygulamasında güvenlik ayarı Yüksek olarak ayarlansa bile çalışır. .NET derleme kod güvenliği, Microsoft Office tarafından değil, Microsoft .NET Framework tarafından yönetilen olmasıdır.  
  
 Ancak, kod çalıştırmadan bir belgeyi açmak için ne zaman isteyebileceğiniz zamanlar vardır. Örneğin, belge açıldığında çalıştırılan kod içeriği değiştirebilir, ancak önce kod değişiklikleri, belgenin görünümünü güncelleştirmek istediğiniz. Belirli bilgiler belge içinde göndermek isteyebilirsiniz veya kod çalıştırın ve büyük olasılıkla içeriği alter istiyor musunuz.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
 Bir belge veya bütünleştirilmiş kodu çalıştırmadan yönetilen kod uzantıları içeren çalışma kitabını açmak için birkaç yolu vardır.  
  
## <a name="to-bypass-the-assembly-by-using-the-shift-key"></a>Shift tuşunu kullanarak derleme atlamak için  
  
-   Açık belgeler ve çalışma kitaplarından **dosya** menüsünü tutarken **Shift** Word ve Excel belge açılırken başlatma olayları oluşturma önlemek için anahtarı.  
  
    > [!NOTE]  
    >  Bir belge veya çalışma kitabından açarsanız **Başlarken** görev bölmesi, basılı **Shift** kodu atlamaz. Ayrıca SHIFT tuşunu basılı olayları belge açıldıktan sonra gerçekleştirilen engellemez.  
  
     Bu yöntem, kodu çalıştıran ve belgeyi değiştirmeden olmadan değişiklik yapmak için bir belge açmak istiyorsanız kullanışlıdır.  
  
## <a name="to-bypass-an-assembly-by-renaming-or-removing-it"></a>Yeniden adlandırma veya kaldırmadan bir derlemenin atlamak için  
  
-   Derleme bulunduğu bilgisayarda gerekli izinlere sahipseniz, yeniden adlandırabilir veya belge veya çalışma kitabı bulunamıyor derlemeyi kaldırın. Bu, Office belge her açıldığında gerçekleştirilen hatayla sonuçlanır.  
  
     Çözüm, birden çok kişi tarafından kullanılıyorsa, bu yöntem çözümü için tümünün çalışmasını engeller. Bu sorun kod veya başvurulan bir sunucu bulunan ve tüm kullanıcıların yürütme engellemek istiyorsanız yararlı olabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Office çözümleri güvenliğini sağlama](../vsto/securing-office-solutions.md)   
 [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)   
 [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)   
 [Office çözümlerinde uygulama ve dağıtım bildirimleri](../vsto/application-and-deployment-manifests-in-office-solutions.md)  
  
  