---
title: 'Nasıl yapılır: Proje bağımlılıklarını oluşturma ve kaldırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- VS.ProjectDependenciesDlg
helpviewer_keywords:
- vs.build.projectdependencies
- project dependencies
- builds [Visual Studio], setting up
- project build configurations, dependencies
- dependencies, project
- projects [Visual Studio], dependencies
ms.assetid: e2a0a8ff-dae7-40a8-b774-b88aa5235183
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 26857824cac478936837a125068bd610dfc4c837
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60117635"
---
# <a name="how-to-create-and-remove-project-dependencies"></a>Nasıl yapılır: Proje Bağımlılıklarını Oluşturma ve Kaldırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Birden çok proje içeren bir çözüm derlerken, belirli projeleri ilk oluşturulacak, diğer projeleri tarafından kullanılan kodu oluşturmak için gerekli olabilir. Bir proje başka bir proje tarafından oluşturulan yürütülebilir kodu kullanırken, kodu oluşturan proje kodu kullanan projenin proje bağımlılık olarak adlandırılır. Bu bağımlılık ilişkiler tanımlanabilir **proje bağımlılıkları** iletişim kutusu.  
  
### <a name="to-assign-dependencies-to-projects"></a>Bağımlılıkları projelerine atamak için  
  
1. Çözüm Gezgini'nde bir proje seçin.  
  
2. Üzerinde **proje** menüsünde seçin **proje bağımlılıkları**.  
  
    **Proje bağımlılıkları** iletişim kutusu açılır.  
  
   > [!NOTE]
   >  **Proje bağımlılıkları** seçeneği, yalnızca kullanılabilir birden fazla proje içeren bir çözümde.  
  
3. Üzerinde **bağımlılıkları** sekmesinde, bir proje seçin **proje** açılan menüsü.  
  
4. İçinde **bağlıdır** alanında, bu proje önce oluşturmanız gerekir, başka bir projeye ait onay kutusunu seçin.  
  
   Proje bağımlılıkları oluşturmadan önce çözümünüzü birden fazla proje oluşmalıdır.  
  
### <a name="to-remove-dependencies-from-projects"></a>Proje bağımlılıkları kaldırmak için  
  
1. Çözüm Gezgini'nde bir proje seçin.  
  
2. Üzerinde **proje** menüsünde seçin **proje bağımlılıkları**.  
  
     **Proje bağımlılıkları** iletişim kutusu açılır.  
  
    > [!NOTE]
    >  **Proje bağımlılıkları** seçeneği, yalnızca kullanılabilir birden fazla proje içeren bir çözümde.  
  
3. Üzerinde **bağımlılıkları** sekmesinde, bir proje seçin **proje** açılan menüsü.  
  
4. İçinde **bağlıdır** alan, bu projenin bağımlılıklarıdır artık herhangi bir projeyi yanındaki onay kutularını temizleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Projeleri ve Visual Studio çözümleri oluşturma ve temizleme](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)   
 [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)   
 [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)   
 [NIB nasıl yapılır: Proje özellikleri ve yapılandırma ayarlarını değiştirme](http://msdn.microsoft.com/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)
