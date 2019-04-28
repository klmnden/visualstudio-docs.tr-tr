---
title: 'Nasıl yapılır: Aynı anda birden fazla yapılandırma derleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: ba830937-3317-4674-8cc2-c0cd565603c5
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 6812395046222c3370e43bfbe75a0502d2cb9044
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63439281"
---
# <a name="how-to-build-multiple-configurations-simultaneously"></a>Nasıl yapılır: Aynı Anda Birden Fazla Yapılandırmayı Derleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Birden çok proje veya bile tüm yapı yapılandırmalarına aynı anda birçok türü kullanarak oluşturabilirsiniz **Toplu derleme** iletişim kutusu. Ancak, aynı anda birden çok oluşturma yapılandırmasında projeleri aşağıdaki türde oluşturulamıyor:  
  
1. [!INCLUDE[win8_appname_long](../includes/win8-appname-long-md.md)] JavaScript kullanarak Windows için oluşturulmuş uygulamalar.  
  
2. Tüm Visual Basic projeleri.  
  
   Derleme yapılandırmaları hakkında daha fazla bilgi için bkz. [derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md).  
  
### <a name="to-build-a-project-in-multiple-build-configurations"></a>Birden çok oluşturma yapılandırmasında bir proje oluşturmak için  
  
1. Menü çubuğunda, **derleme**, **Toplu derleme**.  
  
2. İçinde **derleme** onay kutularını bir projeyi derlemek istediğiniz yapılandırmaları için sütun seçin.  
  
    > [!TIP]
    > Çözüm yapı yapılandırması oluşturun veya düzenlemek için seçin **derleme**, **Configuration Manager** açmak için menü çubuğunda **Configuration Manager** iletişim kutusu. Bir çözüm için bir derleme yapılandırması düzenledikten sonra seçin **yeniden** düğmesine **Toplu derleme** derleme yapılandırmaları Çözümdeki projeler için tüm güncelleştirmek için iletişim kutusu.  
  
3. Seçin **derleme** veya **yeniden** belirttiğiniz yapılandırmaları olan bir projeyi derlemek için düğmeler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)   
 [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)   
 [Paralel Olarak Birden Çok Proje Derleme](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)
