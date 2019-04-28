---
title: C++ için CTest kullanma
ms.date: 11/07/2017
ms.topic: conceptual
ms.author: mblome
manager: jillfra
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: 6be079a5adfe52a7ac750f6713672dad50c7d2a4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62945394"
---
# <a name="how-to-use-ctest-for-c-in-visual-studio"></a>Visual Studio'da C++ için CTest kullanma

(Kod CTest içerir) CMake tümleşik Visual Studio IDE'ye varsayılan olarak **C++ ile masaüstü geliştirme** iş yükü. Makinenizde yüklemeniz gerekiyorsa, Visual Studio yükleyicisi programını açın, **Değiştir** düğmesine ve ardından denetleyin [Visual C++ için CMake araçlarını](/cpp/ide/cmake-tools-for-visual-cpp) altında iş yükü bileşenlerin listesi.

## <a name="to-write-tests"></a>Testler yazmak için

Visual Studio'da CMake desteği, Visual Studio Proje sistemi kullanılmaz. Bu nedenle, yazma ve herhangi bir CMake ortamında olduğu gibi CTest testler yapılandırın. Visual Studio'da CMake kullanma hakkında daha fazla bilgi için bkz. [Visual C++ için CMake araçlarını](/cpp/ide/cmake-tools-for-visual-cpp).

## <a name="to-run-tests"></a>Testleri çalıştırmak için

::: moniker range="vs-2017"

### <a name="visual-studio-2017-version-156-and-later"></a>Visual Studio 2017 sürüm 15.6 ve üzeri

Visual Studio 2017 sürüm 15.6 ve üzeri, CTest tam olarak tümleşiktir **Test Gezgini** ve aynı zamanda Google ve Boost birim testi çerçevelerini destekler. Bu çerçeveler bileşen olarak varsayılan olarak dahil **C++ ile masaüstü geliştirme** iş yükü. Ancak, bir projeyi Visual Studio'nun eski bir sürümden yükseltiyorsanız, Visual Studio yükleyicisi programını kullanarak bu çerçeveleri yüklemeniz gerekebilir.

Aşağıdaki çizim bir CTest, Google Test çerçevesini kullanarak çalıştırma sonuçları gösterilmektedir:

![Visual Studio 2017'de Google Test Çerçevesi ile CTest](media/ctest-test-explorer.png)

CTest ancak değil Google veya Boost bağdaştırıcıları kullanıyorsanız, yöntem düzeyine test sonuçları yerine tek tek CTest düzeyinde bakın. Hata ayıklaması yapabilirsiniz ve adım adım yalnızca CTest yürütülebilir dosyaları, ancak yığın izlemelerini bireysel testler üzerinde desteklenmez.

### <a name="visual-studio-2017-version-155"></a>Visual Studio 2017 sürüm 15.5

Visual Studio 2017 sürüm 15.5, CTest ile tümleşik olmayan **Test Gezgini**. Testlerinizi CMake ana menüden ya da sağ tıklatma menüsünden çalıştırabileceğiniz bir *CMakeLists.txt* dosyası **Çözüm Gezgini**. Test sonuçları için Visual Studio yönlendirilmiş **çıkış penceresine**.

![Visual Studio 2017 sürüm 15.5 CTest testler](media/cpp-cmake-run-tests.png)

::: moniker-end

::: moniker range=">=vs-2019"

CTest ile tam entegredir **Test Gezgini** ve aynı zamanda Google ve Boost birim testi çerçevelerini destekler. Bu çerçeveler bileşen olarak varsayılan olarak dahil **C++ ile masaüstü geliştirme** iş yükü. Ancak, bir projeyi Visual Studio'nun eski bir sürümden yükseltiyorsanız, Visual Studio yükleyicisi programını kullanarak bu çerçeveleri yüklemeniz gerekebilir.

Aşağıdaki çizim bir CTest, Google Test çerçevesini kullanarak çalıştırma sonuçları gösterilmektedir:

![Visual Studio'da Google Test Çerçevesi ile CTest](media/ctest-test-explorer.png)

CTest ancak değil Google veya Boost bağdaştırıcıları kullanıyorsanız, yöntem düzeyine test sonuçları yerine tek tek CTest düzeyinde bakın. Hata ayıklaması yapabilirsiniz ve adım adım yalnızca CTest yürütülebilir dosyaları, ancak yığın izlemelerini bireysel testler üzerinde desteklenmez.

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md)