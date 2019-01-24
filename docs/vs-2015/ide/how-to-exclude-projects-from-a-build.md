---
title: 'Nasıl yapılır: Projeleri derlemeden hariç tutma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 04a3a45af932a34b89feb2726e7a137ceea2ac5a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54780132"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Nasıl yapılır: Projeleri Derlemeden Hariç Tutma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçerdiği tüm projeleri oluşturmaya gerek kalmadan, bir çözüm oluşturabilirsiniz. Örneğin, yapı sonları bir proje hariç. Sorunları araştırmak, sonra projeyi ve adresi ardından oluşturabilirsiniz.  
  
 Bir proje, aşağıdaki yaklaşımlardan yararlanarak dışlayabilirsiniz:  
  
- Etkin çözüm yapılandırmasını geçici olarak kaldırma.  
  
- Bir çözüm yapılandırması oluşturma, proje içermez.  
  
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
 [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)   
 [Nasıl yapılır: Aynı anda birden fazla yapılandırma derleme](../ide/how-to-build-multiple-configurations-simultaneously.md)
