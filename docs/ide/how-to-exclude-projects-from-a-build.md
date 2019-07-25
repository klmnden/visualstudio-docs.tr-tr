---
title: 'Nasıl yapılır: Projeleri derlemeden hariç tutma'
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: conceptual
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 54e65c411afe9815696112dfbcc99bcb9433c4db
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416872"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Nasıl yapılır: Projeleri derlemeden hariç tutma

Bir çözümü, içerdiği tüm projeleri oluşturmadan oluşturabilirsiniz. Örneğin, derlemeyi kesen bir projeyi dışlayabilirsiniz. Ardından, sorunları araştırıp ve adresledikten sonra projeyi derleyebilirsiniz.

Aşağıdaki yaklaşımlardan yararlanarak bir projeyi hariç bırakabilirsiniz:

- Etkin çözüm yapılandırmasından geçici olarak kaldırılıyor.

- Projeyi içermeyen bir çözüm yapılandırması oluşturma.

Daha fazla bilgi için bkz. [derleme yapılandırmasını anlama](../ide/understanding-build-configurations.md).

## <a name="to-temporarily-remove-a-project-from-the-active-solution-configuration"></a>Etkin çözüm yapılandırmasından bir projeyi geçici olarak kaldırmak için

1. Menü çubuğunda**Configuration Manager** **Oluştur** > ' u seçin.

2. **Proje bağlamları** tablosunda, derlemeden dışlamak istediğiniz projeyi bulun.

3. Projenin **Build** sütununda, onay kutusunun işaretini kaldırın.

4. **Kapat** düğmesini seçin ve çözümü yeniden derleyin.

## <a name="to-create-a-solution-configuration-that-excludes-a-project"></a>Projeyi dışlayan bir çözüm yapılandırması oluşturmak için

1. Menü çubuğunda**Configuration Manager** **Oluştur** > ' u seçin.

2. **Etkin çözüm yapılandırması** listesinde  **\<yeni >** ' yi seçin.

3. **Ad** kutusuna çözüm yapılandırması için bir ad girin.

4. **Ayarları Şuradan Kopyala** listesinden, yeni yapılandırmayı temel almak istediğiniz çözüm yapılandırmasını seçin (örneğin, **hata ayıklama**) ve sonra **Tamam** düğmesini seçin.

5. **Configuration Manager** iletişim kutusunda, dışlamak Istediğiniz projenin **Build** sütunundaki onay kutusunun Işaretini kaldırın ve sonra **Kapat** düğmesini seçin.

6. **Standart** araç çubuğunda, yeni çözüm yapılandırmasının **çözüm yapılandırmaları** kutusunda etkin yapılandırma olduğunu doğrulayın.

7. Menü çubuğunda, **derleme** > **çözümü yeniden derle**.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md)
- [Nasıl yapılır: Yapılandırma oluşturma ve düzenleme](../ide/how-to-create-and-edit-configurations.md)
- [Nasıl yapılır: Aynı anda birden çok yapılandırma oluşturun](../ide/how-to-build-multiple-configurations-simultaneously.md)