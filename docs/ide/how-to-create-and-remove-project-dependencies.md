---
title: 'Nasıl yapılır: Proje bağımlılıklarını oluşturma ve kaldırma'
ms.date: 06/21/2017
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
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 476e72e50ac796412fbeef1c180a3340764fb121
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907666"
---
# <a name="how-to-create-and-remove-project-dependencies"></a>Nasıl yapılır: Proje bağımlılıklarını oluşturma ve kaldırma

Birden çok proje içeren bir çözüm derlerken, belirli projeleri ilk oluşturulacak, diğer projeleri tarafından kullanılan kodu oluşturmak için gerekli olabilir. Bir proje başka bir proje tarafından oluşturulan yürütülebilir kodu kullanırken, kodu oluşturan proje kodu kullanan projenin proje bağımlılık olarak adlandırılır. Bu bağımlılık ilişkiler tanımlanabilir **proje bağımlılıkları** iletişim kutusu.

## <a name="to-assign-dependencies-to-projects"></a>Bağımlılıkları projelerine atamak için

1. İçinde **Çözüm Gezgini**, bir proje seçin.

2. Üzerinde **proje** menüsünde seçin **proje bağımlılıkları**.

    **Proje bağımlılıkları** iletişim kutusu açılır.

   > [!NOTE]
   > **Proje bağımlılıkları** seçeneği, yalnızca kullanılabilir birden fazla proje içeren bir çözümde.

3. Üzerinde **bağımlılıkları** sekmesinde, bir proje seçin **proje** açılan menüsü.

4. İçinde **bağlıdır** alanında, bu proje önce oluşturmanız gerekir, başka bir projeye ait onay kutusunu seçin.

   Proje bağımlılıkları oluşturmadan önce çözümünüzü birden fazla proje oluşmalıdır.

## <a name="to-remove-dependencies-from-projects"></a>Proje bağımlılıkları kaldırmak için

1.  İçinde **Çözüm Gezgini**, bir proje seçin.

2.  Üzerinde **proje** menüsünde seçin **proje bağımlılıkları**.

     **Proje bağımlılıkları** iletişim kutusu açılır.

    > [!NOTE]
    > **Proje bağımlılıkları** seçeneği, yalnızca kullanılabilir birden fazla proje içeren bir çözümde.

3.  Üzerinde **bağımlılıkları** sekmesinde, bir proje seçin **proje** açılan menüsü.

4.  İçinde **bağlıdır** alan, bu projenin bağımlılıklarıdır artık herhangi bir projeyi yanındaki onay kutularını temizleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme ve temizleme projeleri ve Visual Studio çözümleri](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)
- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)
- [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)
- [Proje ve çözüm özelliklerini yönetme](managing-project-and-solution-properties.md)