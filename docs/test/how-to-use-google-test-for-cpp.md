---
title: Google Test için C++ kullanma
description: Visual Studio 'da birim C++ testleri oluşturmak için Google test kullanın.
ms.date: 05/06/2017
ms.topic: conceptual
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: 73f62e8b74864af0292a9cc3ab1eb325d679d2ea
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926759"
---
# <a name="how-to-use-google-test-for-c-in-visual-studio"></a>Visual Studio'da C++ için Google Test kullanma

Visual Studio 2017 ve üzeri sürümlerde Google test, Visual Studio IDE **ile birlikte C++**  iş yüküyle masaüstü geliştirmenin varsayılan bir bileşeni olarak tümleşiktir. Makinenizde yüklü olduğunu doğrulamak için Visual Studio Yükleyicisi'ni açın ve Google Test altında iş yükü bileşenlerin listesini bulun:

![Google Test yükle](media/cpp-google-component.png)

::: moniker range="vs-2019"

## <a name="add-a-google-test-project-in-visual-studio-2019"></a>Visual Studio 2019 ' de Google Test projesi ekleme

1. **Çözüm Gezgini**, çözüm düğümüne sağ tıklayıp **Yeni proje** **Ekle** > ' yi seçin.
2. Arama kutusuna dili **C++** olarak ayarlayın ve **Test** yazın. Sonuçlar listesinden **Google test proje**' yi seçin.
3. Test projesi bir ad verin ve tıklayın **Tamam**.

![Yeni Google Test projesi](media/vs-2019/cpp-gtest-new-project-vs2019.png)

::: moniker-end

::: moniker range="vs-2017"

## <a name="add-a-google-test-project-in-visual-studio-2017"></a>Visual Studio 2017 ' de Google Test projesi ekleme

1. **Çözüm Gezgini**, çözüm düğümüne sağ tıklayıp **Yeni proje** **Ekle** > ' yi seçin.
2. Sol bölmede, > **görsel C++**  **Test** ' i seçin ve ardından orta bölmeden **Google test proje** ' yi seçin.
3. Test projesi bir ad verin ve tıklayın **Tamam**.

![Yeni Google Test projesi](media/cpp-gtest-new-project.png)

::: moniker-end

## <a name="configure-the-test-project"></a>Test projesi yapılandırma

İçinde **Test proje yapılandırması** görüntülenen iletişim kutusunda, test etmek istediğiniz projeye seçebilirsiniz. Bir proje seçtiğinizde, Visual Studio Seçili projeye bir başvuru ekler. Hiçbir proje seçerseniz, test etmek istediğiniz projeleri başvuruları el ile eklemeniz gerekir. Statik ve dinamik Google Test ikili dosyalarına bağlanma arasında seçim yaparken, konuları herhangi bir C++ programı ile aynıdır. Daha fazla bilgi için [Visual C++'ta DLL'ler](/cpp/build/dlls-in-visual-cpp).

![Google Test projesi yapılandırma](media/cpp-gtest-config.png)

## <a name="set-additional-options"></a>Ek seçeneklerini ayarlama

Ana menüden **Araçları** > **seçenekleri** > **Google Test için Test bağdaştırıcısı** ek seçeneklerini ayarlamak için. Bu ayarlar hakkında daha fazla bilgi için Google Test belgelerine bakın.

![Google Test projesi ayarları](media/cpp-gtest-settings.png)

## <a name="add-include-directives"></a>Ekleme yönergelerinde

Testinizde *.cpp* dosya, gerekli ekleyin `#include` programınızın türleri ve işlevleri test kodu görünür yapmak için yönergeleri. Genellikle, bir düzey klasör hiyerarşisindeki bir programdır. Yazarsanız `#include "../"` IntelliSense penceresi görünür ve üstbilgi dosyasının tam yolunu seçin olanak sağlar.

![Ekle #include](media/cpp-gtest-includes.png)

## <a name="write-and-run-tests"></a>Yazma ve testleri çalıştırma

Artık yazmak ve Google testleri çalıştırmak hazır olursunuz. Bkz: [Google Test öncü](https://github.com/google/googletest/blob/master/googletest/docs/primer.md) test makrolar hakkında daha fazla bilgi için. Bkz: [Test Gezgini ile birim testleri çalıştırma](run-unit-tests-with-test-explorer.md) kullanarak testlerinizi gruplandırma bulma ve çalıştırma hakkında bilgi için **Test Gezgini**.

## <a name="see-also"></a>Ayrıca bkz.

[C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md)
