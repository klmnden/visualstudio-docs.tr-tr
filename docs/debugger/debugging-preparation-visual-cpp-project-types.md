---
title: C++ projelerinde hata ayıklamak hazırlama | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- project templates, debugging
- Visual C++ projects, debugging
- debug builds, project settings
- debugging [C++]
ms.assetid: 912b4ba2-7719-43d5-b087-db33e3f9329a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: abc3a8339fffab762c2b6d7a649d3bae8efa76c8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925496"
---
# <a name="debugging-preparation-visual-c-project-types"></a>Hata Ayıklama Hazırlığı: Visual C++ Proje Türleri
Bu bölümde oluşturan temel proje türlerinde hata ayıklama işlemini açıklamaktadır [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] proje şablonları.

 Proje türlerine çıktılarını DLL'leri oluşturma halinde gruplandırılır Not [DLL projelerinde hata ayıklama](../debugger/debugging-dll-projects.md) paylaştıkları genel özellikleri nedeniyle.

## <a name="BKMK_In_this_topic"></a> Bu konudaki
 [Önerilen özellik ayarları](#BKMK_Recommended_Property_Settings)

 [Win32 projeleri](#BKMK_Win32_Projects)

- [Bir C veya C++ Win32 uygulamasında hata ayıklamak için](#BKMK_To_debug_a_C_or_C___Win32_application)

- [Hata ayıklama yapılandırmasını el ile ayarlamak için](#BKMK_To_manually_set_a_Debug_configuration)

  [Windows Forms uygulamaları (.NET)](#BKMK_Windows_Forms_Applications___NET_)

## <a name="BKMK_Recommended_Property_Settings"></a> Önerilen özellik ayarları
 Bazı özellikler tüm yönetilmeyen hata ayıklama senaryoları için aynı şekilde ayarlamanız gerekir. Aşağıdaki tablolarda, önerilen özellik ayarları gösterilmiştir. Burada listelenmeyen ayarlar, yönetilmeyen farklı proje türleri arasında değişebilir. Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md).

### <a name="configuration-properties-124-cc-124-optimization-node"></a>Yapılandırma özellikleri &#124; C/C++ &#124; iyileştirme düğümü

|Özellik adı|Ayar|
|-------------------|-------------|
|**En iyi duruma getirme**|Kümesine **devre dışı (/ 0 d).** Oluşturulan yönergeler doğrudan sizin kaynak kodunuza karşılık gelmediğinden en iyi duruma getirilmiş kod hatalarını ayıklamak için zordur. Programınızda, yalnızca en iyi duruma getirilmiş kodda görüntülenen bir hata bulursanız, bu ayarı açabilirsiniz, ancak gösterilen kodun **ayrıştırılmış kodu** penceresi, kaynak kodunuzda gördüğünüz eşleşmeyebilir en iyi duruma getirilmiş kaynaktan oluşturulur Windows. Adımlama gibi diğer özellikleri beklendiği gibi çalışmayabilir.|

### <a name="configuration-properties-124-linker-124-debugging-node"></a>Yapılandırma özellikleri &#124; bağlayıcı &#124; hata ayıklama düğümü

|Özellik adı|Ayar|
|-------------------|-------------|
|**Hata ayıklama bilgileri üret**|Her zaman bu seçeneği ayarlamalısınız **Evet (/ DEBUG)** hata ayıklama sembolleri ve hata ayıklama için gereken dosyaları oluşturmak için. Uygulama üretime gittiğinde, off olarak ayarlayabilirsiniz.|

 [Bu konudaki](../debugger/debugging-preparation-visual-cpp-project-types.md#BKMK_In_this_topic)

## <a name="BKMK_Win32_Projects"></a> Win32 projeleri
 Win32, C veya C++ ile yazılmış geleneksel Windows programları uygulamalardır. Bu tür bir uygulamada hata ayıklama [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] oldukça basittir.

 MFC ve ATL Projelerimi Win32 uygulamaları içerir. Windows API'larını kullanın ve MFC veya ATL kullanabilir, ancak ortak dil çalışma zamanı (CLR) kullanmayın. Ancak, CLR kullanan yönetilen kodu çağrısı olabilir.

 Aşağıdaki yordam, içinden bir Win32 Proje hatalarını ayıklamaya açıklanmaktadır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Dışında uygulamayı başlatmak için bir Win32 uygulamasında hata ayıklamak için başka bir yolu olan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ve ekleyebilir. Daha fazla bilgi için [çalışan işlemlere ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).

### <a name="BKMK_To_debug_a_C_or_C___Win32_application"></a> Bir C veya C++ Win32 uygulamasında hata ayıklamak için

1. Projeyi Visual Studio'da açın.

2. Üzerinde **hata ayıklama** menüsünde seçin **Başlat**.

3. Hata [ayıklayıcıyla ilk bakış](../debugger/debugger-feature-tour.md)bölümünde açıklanan teknikleri kullanarak hata ayıklayın.

### <a name="BKMK_To_manually_set_a_Debug_configuration"></a> Hata ayıklama yapılandırmasını el ile ayarlamak için

1. Üzerinde **görünümü** menüsünü tıklatın **özellik sayfaları**.

2. Tıklayın **yapılandırma özellikleri** zaten değilse, açmak için düğümü

3. Seçin **genel**, değerini ayarlayıp **çıkış** için satır **hata ayıklama**.

4. Açık **C/C++** düğüm ve select **genel**.

    İçinde **hata ayıklama** satır derleyici tarafından oluşturulacak hata ayıklama türünü belirtin. Seçtiğiniz değerler **Program veritabanı (/Zi)** veya **Düzenle ve devam et (/zı) için Program veritabanı**.

5. Seçin **iyileştirme**hem de **iyileştirme** satır, select **devre dışı (/ 0d)** aşağı açılan listeden.

    Oluşturulan yönergeler doğrudan sizin kaynak kodunuza karşılık gelmediğinden en iyi duruma getirilmiş kod hatalarını ayıklamak için zordur. Programınızda, yalnızca en iyi duruma getirilmiş kodda görüntülenen bir hata bulursanız, bu ayarı açabilirsiniz, ancak ayrıştırma penceresinde gösterilen kodun kaynak pencerelerinizi gördüğünüz eşleşmeyebilir en iyi duruma getirilmiş kaynaktan oluşturulduğunu unutmayın. Adımlama gibi özellikleri, kesme noktaları ve yürütme yanlış noktası gösterilecek olasıdır.

6. Açık **bağlayıcı** düğüm ve select **hata ayıklama**. İlk **Oluştur** satır, select **Evet (/ DEBUG)** aşağı açılan listeden. Her zaman hata ayıklaması yapıyorsanız bu ayarlar.

   Daha fazla bilgi için[C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md).

   [Bu konudaki](../debugger/debugging-preparation-visual-cpp-project-types.md#BKMK_In_this_topic)

## <a name="BKMK_Windows_Forms_Applications___NET_"></a> Windows Forms uygulamaları (.NET)
 **Windows Forms uygulaması (.NET)** şablon oluşturur bir [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] Windows Forms uygulaması. Daha fazla bilgi için [nasıl yapılır: Windows uygulama projesi](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/42wc9kk5(v=vs.100))oluşturun.

 Bu tür bir uygulamada hata ayıklama [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] yönetilen Windows Forms uygulamalarında benzer.

 Proje şablonuyla bir Windows Forms projesi oluşturduğunuzda [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] hata ayıklama ve yayın yapılandırmaları için gereken ayarları otomatik olarak oluşturur. Gerekirse, bu ayarları değiştirip değiştiremeyeceğini  **\<proje adı > özellik sayfaları** iletişim kutusu. Daha fazla bilgi için [hata ayıklama ve yayın yapılandırmaları](../debugger/how-to-set-debug-and-release-configurations.md).

 Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md).

 Dışında uygulamayı başlatmak için bir Windows Forms uygulamasında hata ayıklamak için başka bir yolu olan [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ve ekleyebilir. Daha fazla bilgi için [bir çalışan bir Program veya birden çok programları ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).

 [Bu konudaki](../debugger/debugging-preparation-visual-cpp-project-types.md#BKMK_In_this_topic)

## <a name="see-also"></a>Ayrıca Bkz.
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [C++ Hata Ayıklama Yapılandırması Proje Ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)
- [Çalışan bir programa veya birden çok programa ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)
- [Hata ayıklama ve sürüm yapılandırması](../debugger/how-to-set-debug-and-release-configurations.md)
- [Nasıl yapılır: Windows uygulama projesi oluşturma](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/42wc9kk5(v=vs.100))