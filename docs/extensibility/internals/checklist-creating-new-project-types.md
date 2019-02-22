---
title: 'Denetim listesi: Yeni proje türleri oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], creating new types
- project types, checklist for creating
ms.assetid: 29eb9c3b-1933-4741-aa85-65a33f0825ba
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 336c7a98a3c03f63b74cefa3ab3a4586408cfccf
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621012"
---
# <a name="checklist-create-new-project-types"></a>Denetim listesi: Yeni proje türleri oluşturma
Yeni bir proje türü oluşturmak için birkaç görevi tamamlamanız gerekir. Aşağıdaki denetim listesinde, bu görevleri için bir kılavuz sağlar:

1.  Yeni Proje türünüz için işlevsellik tasarlayın. Daha fazla bilgi için [proje türü tasarım kararları](../../extensibility/internals/project-type-design-decisions.md).

2.  Hangi düzenleyicileri, kod ve diğer proje öğeleri için kullanıldığını belirleyebilirsiniz. Temel veya standart düzenleyicileri kullanabilirsiniz ya da oluşturabilir ve projeye özgü düzenleyicileri kullanır. Daha fazla bilgi için [özel düzenleyiciler ve tasarımcılar oluşturma](../../extensibility/creating-custom-editors-and-designers.md) ve [nasıl yapılır: Projeye özgü düzenleyicileri açma](../../extensibility/how-to-open-project-specific-editors.md).

3.  Proje öğelerinizi olacaktır katılım düzeyini belirlemek **sınıf görünümü** ve **Nesne Tarayıcısı**. Daha fazla bilgi için [sembol tarama araçlarını destekleyen](../../extensibility/internals/supporting-symbol-browsing-tools.md).

4.  Proje ve proje öğeleri için daha önce yapılan tasarım kararlarına göre yeni bir sınıf türetin.

5.  Aşağıdaki proje türü bileşenler için kodu yazın:

    -   Yeni proje oluşturma ve mevcut projeleri açma yönetmek için proje üreteci. Daha fazla bilgi için [proje üreteçlerini kullanarak proje örnekleri oluşturma](../../extensibility/internals/creating-project-instances-by-using-project-factories.md).

    -   Proje hiyerarşisi ve komut işleme. Daha fazla bilgi için [bir proje türü (C++) uygulamak için kullanım HierUtil7 proje sınıfları](https://msdn.microsoft.com/library/a5c16a09-94a2-46ef-87b5-35b815e2f346), [proje modeli öğeleri](../../extensibility/internals/elements-of-a-project-model.md), [proje modeli çekirdek bileşenleri](../../extensibility/internals/project-model-core-components.md)ve [ MenuCommands vs. OleMenuCommands](../../extensibility/menucommands-vs-olemenucommands.md).

    -   Proje öğeleri yönetimi, projenize ekleme dahil olmak üzere **yeni proje** iletişim kutusu. Daha fazla bilgi için [proje ve proje öğesi şablonları ekleme](../../extensibility/internals/adding-project-and-project-item-templates.md) ve [proje ve öğe şablonlarını kaydetme](../../extensibility/internals/registering-project-and-item-templates.md).

    -   Kalıcılık proje durumu ve tek tek öğeleri. Daha fazla bilgi için [açık proje öğeleri kaydedip](../../extensibility/internals/opening-and-saving-project-items.md). Çözüm bilgileri kalıcılığını bkz [çözümleri](../../extensibility/internals/solutions.md).

    -   Özellikler penceresinde görüntülemek için yapılandırma bağımsız Özellikleri'ni kullanın. Daha fazla bilgi için [özellikleri genişletmenize](../../extensibility/internals/extending-properties.md).

    -   Bağımlı yapılandırma özelliklerini göstermek için özellik sayfaları'nda uygulandığı şekilde proje yapılandırma özellikleri. Daha fazla bilgi için [yapılandırma seçeneklerini yönetme](../../extensibility/internals/managing-configuration-options.md).

    -   Dağıtım için çıktı numaralandırma. Daha fazla bilgi için [çıkış için proje yapılandırması](../../extensibility/internals/project-configuration-for-output.md).

    -   Proje başlangıç Hizmetleri. Daha fazla bilgi için [proje modeli öğeleri](../../extensibility/internals/elements-of-a-project-model.md) ve [proje modeli çekirdek bileşenleri](../../extensibility/internals/project-model-core-components.md).

    -   Nesneleri veya türetilmiş sınıflar `IDispatch`, otomasyon için kullanılabilir.

    -   XML komut tablosu (*.vsct*) dosyaları. Daha fazla bilgi için [Visual Studio komut tablosu (.vsct) dosyaları](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md).

6.  Test, hata ayıklama ve başlatma, proje türü.

7.  Projenizde görüntülemek **proje** sekmesinde **Başvuru Ekle** ayarlayarak iletişim kutusu `VARIANT_TRUE` değeri olarak `VSHPROPID_ShowProjInSolutionPage`. Daha fazla bilgi için bkz. <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A>.

8.  Microsoft Installer oluşturun (*.msi*), VSPackage yükleme dosyası. Daha fazla bilgi için [Windows Installer ile VSPackage yükleme](../../extensibility/internals/installing-vspackages-with-windows-installer.md), [bir proje türü kaydetme](../../extensibility/internals/registering-a-project-type.md), ve [VSPackages](../../extensibility/internals/vspackages.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio’da Hiyerarşiler](../../extensibility/internals/hierarchies-in-visual-studio.md)
- [Proje türleri oluşturma zamanı](../../extensibility/internals/when-to-create-project-types.md)
- [Proje türleri oluşturma](../../extensibility/internals/creating-project-types.md)