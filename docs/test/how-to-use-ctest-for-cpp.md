---
title: C++ için CTest kullanma
ms.date: 05/01/2019
ms.topic: conceptual
ms.author: mblome
manager: jillfra
ms.workload:
- cplusplus
author: mikeblome
ms.openlocfilehash: 0b6c4eb391014342a18ec3fe56a03a651463105c
ms.sourcegitcommit: d4920babfc3d24a3fe1d4bf446ed3fe73b344467
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2019
ms.locfileid: "67160088"
---
# <a name="how-to-use-ctest-for-c-in-visual-studio-2017-and-later"></a>İçin CTest kullanma C++ Visual Studio 2017 ve üzeri

(Kod CTest içerir) CMake tümleşik Visual Studio IDE'ye varsayılan olarak **C++ ile masaüstü geliştirme** iş yükü. Makinenizde yüklemeniz gerekiyorsa, Visual Studio yükleyicisi programını açın, **ile masaüstü geliştirme C++**  düğmesine ve ardından tıklayın **Değiştir**. Seçin  **C++ Windows için CMake araçlarını** altında iş yükü bileşenlerin listesi.

## <a name="to-write-tests"></a>Testler yazmak için

Visual Studio'da CMake desteği, Visual Studio Proje sistemi kullanılmaz. Bu nedenle, yazma ve herhangi bir CMake ortamında olduğu gibi CTest testler yapılandırın. Visual Studio'da CMake kullanma hakkında daha fazla bilgi için bkz. [Visual Studio'daki CMake projeleri](/cpp/build/cmake-projects-in-visual-studio).

## <a name="to-run-tests"></a>Testleri çalıştırmak için

CTest ile tam entegredir **Test Gezgini** ve aynı zamanda Google ve Boost birim testi çerçevelerini destekler. Bu çerçeveler bileşen olarak varsayılan olarak dahil **C++ ile masaüstü geliştirme** iş yükü. Ancak, bir projeyi Visual Studio'nun eski bir sürümden yükseltiyorsanız, Visual Studio yükleyicisi programını kullanarak bu çerçeveleri yüklemeniz gerekebilir.

Aşağıdaki çizim bir CTest, Google Test çerçevesini kullanarak çalıştırma sonuçları gösterilmektedir:

![Visual Studio'da Google Test Çerçevesi ile CTest](media/ctest-test-explorer.png)

CTest ancak değil Google veya Boost bağdaştırıcıları kullanıyorsanız, yöntem düzeyine test sonuçları yerine tek tek CTest düzeyinde bakın. Hata ayıklaması yapabilirsiniz ve adım adım yalnızca CTest yürütülebilir dosyaları, ancak yığın izlemelerini bireysel testler üzerinde desteklenmez.

Aşağıdaki çizim bir CTest, Google Test çerçevesini kullanarak çalıştırma sonuçları gösterilmektedir:

![Visual Studio 2017'de Google Test Çerçevesi ile CTest](media/ctest-test-explorer.png)

CTest ancak değil Google veya Boost bağdaştırıcıları kullanıyorsanız, yöntem düzeyine test sonuçları yerine tek tek CTest düzeyinde bakın. Hata ayıklaması yapabilirsiniz ve adım adım yalnızca CTest yürütülebilir dosyaları, ancak yığın izlemelerini bireysel testler üzerinde desteklenmez.

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ için birim testleri yazma](writing-unit-tests-for-c-cpp.md)
