---
title: 'Nasıl yapılır: Projeleri hedef birden çok platform için yapılandırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio], targeting platforms
- platforms, changing target platforms
ms.assetid: affa2392-7aed-45ac-9ffa-1d8e0496d590
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7457b5be3a6c1cbf2c2b6a1c6f66f9fb89e8d225
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60100306"
---
# <a name="how-to-configure-projects-to-target-multiple-platforms"></a>Nasıl yapılır: Projeleri Birden Çok Platformu Hedefleyecek Şekilde Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] aynı anda birçok farklı CPU mimarileri veya platformlarını hedeflemek bir çözüm için bir yol sağlar. Ayarlamak için bu özellikleri aracılığıyla erişilen **Configuration Manager** iletişim kutusu.  
  
## <a name="targeting-a-platform"></a>Bir Platform desteği  
 **Configuration Manager** iletişim kutusunda, oluşturmak ve çözüm ve proje düzeyinde yapılandırmalar ve platformlar izin verir. Her bir çözüm düzeyinde yapılandırmaları ve hedefleri bileşimi benzersiz bir hedefleyen arasında kolayca, örneğin, bir sürüm yapılandırması geçiş olanak tanıyan ilişkili özellikler kümesini olabilir bir [!INCLUDE[vcprx64](../includes/vcprx64-md.md)] platform, yayın yapılandırması x x86 hedefleyen platform ve bir x86 hedefleyen bir hata ayıklama yapılandırması platformu.  
  
#### <a name="to-set-your-configuration-to-target-a-different-platform"></a>Farklı bir platform hedeflemek için yapılandırmayı ayarlamak için  
  
1. Üzerinde **derleme** menüsünde tıklatın **Configuration Manager**.  
  
2. İçinde **etkin çözüm platformu kutusu**, çözümünüze hedef istediğiniz ya da seçin platformu seçin  **\<yeni >** yeni platformu oluşturmak için. [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Etkin platform olarak ayarlanmış olan platformunu hedeflemek için uygulamanızı derleyeceği **Configuration Manager** iletişim kutusu.  
  
## <a name="removing-a-platform"></a>Bir Platform kaldırılıyor  
 Gerek bir platform olduğunu fark ederseniz Configuration Manager iletişim kutusunu kullanarak kaldırabilirsiniz. Bu, yapılandırma ve hedef birleşimi için yapılandırdığınız tüm çözüm ve proje ayarlarını kaldırır.  
  
#### <a name="to-remove-a-platform"></a>Bir platform kaldırmak için  
  
1. Üzerinde **derleme** menüsünde tıklatın **Configuration Manager**.  
  
2. İçinde **etkin çözüm platformu kutusu**seçin  **\<Düzenle >**. **Çözüm platformları Düzenle** iletişim kutusu açılır.  
  
3. Kaldırın ve istediğiniz platform tıklayın **Kaldır**.  
  
## <a name="targeting-multiple-platforms-with-one-solution"></a>Bir Çözümle birden çok platformu hedefleme  
 Ayarlarını yapılandırma ve platform ayarları birleşimi göre değişebileceği için birden çok platformu hedefleyen bir çözümünü ayarlayabilirsiniz.  
  
#### <a name="to-target-multiple-platforms"></a>Birden çok platformu hedefleyecek şekilde  
  
1. Kullanım **Configuration Manager** en az iki hedef platformlara çözümü eklemek için.  
  
2. Gelen hedeflemek istediğiniz platformu seçin **etkin çözüm platformu** listesi.  
  
3. Çözümü oluşturun.  
  
#### <a name="to-build-multiple-solution-configurations-at-once"></a>Aynı anda birden çok çözüm yapılandırmaları oluşturmak için  
  
1. Kullanım **Configuration Manager** en az iki hedef platformlara çözümü eklemek için.  
  
2. Kullanım **Toplu derleme** penceresi aynı anda çeşitli çözüm yapılandırmalar da oluşturabilirsiniz.  
  
   Örneğin, ayarlamak için bir çözüm düzeyinde platforma sahip mümkündür [!INCLUDE[vcprx64](../includes/vcprx64-md.md)], ve aynı platform hedefleme, çözüm içinde proje yok. Çözümünüz içinde her farklı platformları hedefleyen birden çok proje mümkündür. Bunlardan biri varsa, Karışıklığı önlemek için açıklayıcı bir ad ile yeni bir yapılandırma oluşturmak önerilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)   
 [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)   
 [Visual Studio'da Projeler ve Çözümler Oluşturma ve Temizleme](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)
