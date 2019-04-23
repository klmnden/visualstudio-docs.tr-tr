---
title: 'Nasıl yapılır: Projeleri derlemeden hariç tutma'
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: conceptual
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24ca736d65a889c0bbada24412ebedecbe6970ce
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60107560"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Nasıl yapılır: Projeleri derlemeden hariç tutma

İçerdiği tüm projeleri oluşturmaya gerek kalmadan, bir çözüm oluşturabilirsiniz. Örneğin, yapı sonları bir proje hariç. Sorunları araştırmak, sonra projeyi ve adresi ardından oluşturabilirsiniz.

Bir proje, aşağıdaki yaklaşımlardan yararlanarak dışlayabilirsiniz:

- Etkin çözüm yapılandırmasını geçici olarak kaldırma.

- Bir çözüm yapılandırması oluşturma, proje içermez.

Daha fazla bilgi için [anlayın derleme yapılandırmaları](../ide/understanding-build-configurations.md).

## <a name="to-temporarily-remove-a-project-from-the-active-solution-configuration"></a>Bir projenin etkin çözüm yapılandırmasını geçici olarak kaldırmak için

1. Menü çubuğunda, **derleme** > **Configuration Manager**.

2. İçinde **proje bağlamları** tablo, derlemeden hariç tutmak istediğiniz proje bulun.

3. İçinde **derleme** sütun proje için onay kutusunu temizleyin.

4. Seçin **Kapat** düğmesini ve ardından çözümü yeniden oluşturun.

## <a name="to-create-a-solution-configuration-that-excludes-a-project"></a>Bir proje dışlayan bir çözüm yapılandırmasını oluşturmak için

1. Menü çubuğunda, **derleme** > **Configuration Manager**.

2. İçinde **etkin çözüm yapılandırması** listesinde  **\<yeni >**.

3. İçinde **adı** kutusuna, çözüm yapılandırması için bir ad girin.

4. İçinde **Ayarları Şuradan Kopyala** listesinde, yeni yapılandırmayı temel almak istediğiniz çözüm yapılandırması seçin (örneğin, **hata ayıklama**) ve ardından **Tamam** düğmesi .

5. İçinde **Configuration Manager** iletişim kutusu, onay kutusunu temizleyin **derleme** sütununu hariç tutun ve ardından istediğiniz proje için **Kapat** düğmesi.

6. Üzerinde **standart** araç, yeni çözüm yapılandırması etkin yapılandırmada olduğundan emin olun **çözüm yapılandırmaları** kutusu.

7. Menü çubuğunda, **derleme** > **çözümü yeniden derle**.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)
- [Nasıl yapılır: Yapılandırmaları oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)
- [Nasıl yapılır: Aynı anda birden fazla yapılandırma derleme](../ide/how-to-build-multiple-configurations-simultaneously.md)