---
title: 'Nasıl yapılır: derlemeden projeleri hariç tutma | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: e1d7bfbf2b12113bd7d80a6dd6af19b4470e30b1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49242859"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Nasıl yapılır: Derlemeden Projeleri Hariç Tutma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçerdiği tüm projeleri oluşturmaya gerek kalmadan, bir çözüm oluşturabilirsiniz. Örneğin, yapı sonları bir proje hariç. Sorunları araştırmak, sonra projeyi ve adresi ardından oluşturabilirsiniz.  
  
 Bir proje, aşağıdaki yaklaşımlardan yararlanarak dışlayabilirsiniz:  
  
-   Etkin çözüm yapılandırmasını geçici olarak kaldırma.  
  
-   Bir çözüm yapılandırması oluşturma, proje içermez.  
  
 Daha fazla bilgi için [derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md).  
  
### <a name="to-temporarily-remove-a-project-from-the-active-solution-configuration"></a>Bir projenin etkin çözüm yapılandırmasını geçici olarak kaldırmak için  
  
1.  Menü çubuğunda, **derleme**, **Configuration Manager**.  
  
2.  İçinde **proje bağlamları** tablo, derlemeden hariç tutmak istediğiniz proje bulun.  
  
3.  İçinde **derleme** sütun proje için onay kutusunu temizleyin.  
  
4.  Seçin **Kapat** düğmesini ve ardından çözümü yeniden oluşturun.  
  
### <a name="to-create-a-solution-configuration-that-excludes-a-project"></a>Bir proje dışlayan bir çözüm yapılandırmasını oluşturmak için  
  
1.  Menü çubuğunda, **derleme**, **Configuration Manager**.  
  
2.  İçinde **etkin çözüm yapılandırması** listesinde  **\<yeni >**.  
  
3.  İçinde **adı** kutusuna, çözüm yapılandırması için bir ad girin.  
  
4.  İçinde **Ayarları Şuradan Kopyala** listesinde, yeni yapılandırmayı temel almak istediğiniz çözüm yapılandırması seçin (örneğin, **hata ayıklama**) ve ardından **Tamam** düğmesi .  
  
5.  İçinde **Configuration Manager** iletişim kutusu, onay kutusunu temizleyin **derleme** sütununu hariç tutun ve ardından istediğiniz proje için **Kapat** düğmesi.  
  
6.  Üzerinde **standart** araç, yeni çözüm yapılandırması etkin yapılandırmada olduğundan emin olun **çözüm yapılandırmaları** kutusu.  
  
7.  Menü çubuğunda, **derleme**, **çözümü yeniden derle**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)   
 [Nasıl yapılır: yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)   
 [Nasıl yapılır: Aynı Anda Birden Fazla Yapılandırma Derleme](../ide/how-to-build-multiple-configurations-simultaneously.md)



