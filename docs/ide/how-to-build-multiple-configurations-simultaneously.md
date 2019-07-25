---
title: 'Nasıl yapılır: Aynı anda birden fazla yapılandırmayı derleme'
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: conceptual
ms.assetid: ba830937-3317-4674-8cc2-c0cd565603c5
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7f4abd95c2a37366b4f6dfabe141e6418d23301d
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416764"
---
# <a name="how-to-build-multiple-configurations-simultaneously"></a>Nasıl yapılır: Aynı anda birden fazla yapılandırmayı derleme

**Toplu Iş oluşturma** iletişim kutusunu kullanarak, aynı anda birden çok proje türünü, yapı yapılandırmalarının birden çok kez veya hatta tamamını oluşturabilirsiniz. Ancak, aynı anda birden çok yapı yapılandırmasında aşağıdaki proje türlerini derleyebilirsiniz:

1. [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)]JavaScript kullanarak Windows için oluşturulmuş uygulamalar.

2. Tüm Visual Basic projeleri.

   Derleme konfigürasyonları hakkında daha fazla bilgi için bkz. [derleme yapılandırmasını anlama](../ide/understanding-build-configurations.md).

## <a name="to-build-a-project-in-multiple-build-configurations"></a>Birden çok yapı yapılandırmasında bir proje oluşturmak için

1. Menü çubuğunda,**Toplu derleme** **Oluştur** > ' u seçin.

2. **Build** sütununda, bir proje derlemek istediğiniz yapılandırmaların onay kutularını seçin.

    > [!TIP]
    > Bir çözüme yönelik derleme yapılandırması düzenlemek veya oluşturmak için, menü çubuğunda**Configuration Manager** **Oluştur** > ' u seçerek **Configuration Manager** iletişim kutusunu açın. Bir çözüm için yapı yapılandırmasını düzenledikten sonra, çözümdeki projelerin tüm derleme yapılandırmalarını güncelleştirmek için **Batch derlemesi** Iletişim kutusundaki **yeniden oluştur** düğmesini seçin.

3. Projeyi belirttiğiniz yapılandırmalara göre derlemek için **Derle** veya **yeniden oluştur** düğmelerini seçin.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Yapılandırma oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)
- [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)
- [Paralel olarak birden çok proje oluşturun](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)