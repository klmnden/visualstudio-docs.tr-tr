---
title: 'Nasıl yapılır: Aynı anda birden fazla yapılandırmayı derleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-compile
ms.topic: conceptual
ms.assetid: ba830937-3317-4674-8cc2-c0cd565603c5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e2edd27174964f1fbddf452a3cb468915d9fc93f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55010278"
---
# <a name="how-to-build-multiple-configurations-simultaneously"></a>Nasıl yapılır: Aynı anda birden fazla yapılandırmayı derleme

Birden çok proje veya bile tüm yapı yapılandırmalarına aynı anda birçok türü kullanarak oluşturabilirsiniz **Toplu derleme** iletişim kutusu. Ancak, aynı anda birden çok oluşturma yapılandırmasında projeleri aşağıdaki türde oluşturulamıyor:

1. [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] JavaScript kullanarak Windows için oluşturulmuş uygulamalar.

2. Tüm Visual Basic projeleri.

   Derleme yapılandırmaları hakkında daha fazla bilgi için bkz. [anlayın derleme yapılandırmaları](../ide/understanding-build-configurations.md).

## <a name="to-build-a-project-in-multiple-build-configurations"></a>Birden çok oluşturma yapılandırmasında bir proje oluşturmak için

1. Menü çubuğunda, **derleme** > **Toplu derleme**.

2. İçinde **derleme** onay kutularını bir projeyi derlemek istediğiniz yapılandırmaları için sütun seçin.

    > [!TIP]
    > Çözüm yapı yapılandırması oluşturun veya düzenlemek için seçin **derleme** > **Configuration Manager** açmak için menü çubuğunda **Configuration Manager** iletişim kutusu. Bir çözüm için bir derleme yapılandırması düzenledikten sonra seçin **yeniden** düğmesine **Toplu derleme** derleme yapılandırmaları Çözümdeki projeler için tüm güncelleştirmek için iletişim kutusu.

3. Seçin **derleme** veya **yeniden** belirttiğiniz yapılandırmaları olan bir projeyi derlemek için düğmeler.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)
- [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)
- [Paralel olarak birden çok proje derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)