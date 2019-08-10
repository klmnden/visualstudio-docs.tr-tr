---
title: C/C++ İçin Kod Analizine Genel Bakış
ms.date: 04/28/2018
ms.topic: conceptual
helpviewer_keywords:
- annotations, code analysis
- build integration, code analysis
- C/C++ code analysis
- IDE, code analysis
- pragma directive, code analysis
- code analysis, C/C++
- code analysis tool
- command line, code analysis
- C++, code analysis
- check-in policies, code analysis
- '#pragma directives, code analysis'
- C, code analysis
ms.assetid: 81f0c9e8-f471-4de5-aac4-99db336a8809
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- cplusplus
ms.openlocfilehash: f7b0e29f6a9a502054b59fc7313c3eff0565f938
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919893"
---
# <a name="code-analysis-for-cc-overview"></a>C/C++ Overview için kod analizi

C/C++ Code çözümleme aracı, c/C++ kaynak kodunuzda olası arızaların bilgilerini sağlar. Araç tarafından bildirilen yaygın kodlama hataları, arabellek taşmaları, Başlatılmamış bellek, null işaretçi başvurusu ve bellek ve kaynak sızıntılarını içerir. Araç ayrıca [ C++ temel yönergelere](http://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md)karşı denetimleri de çalıştırabilir.

## <a name="ide-integrated-development-environment-integration"></a>IDE (tümleşik geliştirme ortamı) Tümleştirmesi

Kod Analizi Aracı, Visual Studio IDE içinde tamamen tümleşiktir.

Yapı işlemi sırasında, kaynak kodu için oluşturulan tüm uyarılar Hata Listesi görüntülenir. Uyarıya neden olan kaynak koda gidebilir ve sorunun nedeni ve olası çözümleriyle ilgili ek bilgileri görüntüleyebilirsiniz.

## <a name="command-line-support"></a>Komut satırı desteği

Aşağıdaki örnekte gösterildiği gibi, komut satırından çözümleme aracını da kullanabilirsiniz:

```cmd
C:\>cl /analyze Sample.cpp
```

**Visual Studio 2017 sürüm 15,7 ve üzeri** Aracı, CMake dahil olmak üzere herhangi bir derleme sistemiyle komut satırından çalıştırabilirsiniz.

## <a name="pragma-support"></a>#pragma desteği

Uyarıları hata olarak değerlendirmek `#pragma` , uyarıları etkinleştirmek veya devre dışı bırakmak ve tek kod satırları için uyarıları gizlemek için yönergesini kullanabilirsiniz. Daha fazla bilgi için bkz. [pragma yönergeleri ve __Pragma Anahtar sözcüğü](https://docs.microsoft.com/cpp/preprocessor/pragma-directives-and-the-pragma-keyword).

## <a name="annotation-support"></a>Ek açıklama desteği

Ek açıklamalar, kod analizinin doğruluğunu geliştirir. Ek açıklamalar, işlev parametreleri ve dönüş türlerinde ön ve son koşullar hakkında ek bilgiler sağlar. Daha fazla bilgi için, bkz. [CC++ /kod HATALARıNı azaltmak Için sal ek açıklamalarını kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md).

## <a name="run-analysis-tool-as-part-of-check-in-policy"></a>İade ilkesinin bir parçası olarak analiz aracını Çalıştır

Tüm kaynak kodu iadelerinin belirli ilkeleri karşıladıklarından emin olmak isteyebilirsiniz. Özellikle, çözümlemenin en son yerel yapıya bir adım olarak çalıştırılmış olduğundan emin olmak istersiniz. Kod Analizi iade ilkesini etkinleştirme hakkında daha fazla bilgi için bkz. [Kod Analizi Iade Ilkeleri oluşturma ve kullanma](../code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies.md).

## <a name="team-build-integration"></a>Takım derlemesi tümleştirmesi

Yapı işleminin bir adımı [!INCLUDE[esprtfs](../code-quality/includes/esprtfs_md.md)] olarak kod analizi aracını çalıştırmak için derleme sisteminin tümleşik özelliklerini kullanabilirsiniz. Daha fazla bilgi için [Azure işlem hatları](/azure/devops/pipelines/index?view=vsts).

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Başlangıç: C/için kod analiziC++](quick-start-code-analysis-for-c-cpp.md)
- [İzlenecek yol: Hatalar için CC++ /kodu çözümle](walkthrough-analyzing-c-cpp-code-for-defects.md)
- [C/C++ İçin Kod Analizi Uyarıları](code-analysis-for-c-cpp-warnings.md)
- [C++ Temel Yönergeleri denetleyicilerini kullanma](using-the-cpp-core-guidelines-checkers.md)
- [C++Temel kılavuz denetleyicisi başvurusu](code-analysis-for-cpp-corecheck.md)
- [Çalıştırılacak C++ Kurallarını Belirtmek için Kural Kümeleri Kullanma](using-rule-sets-to-specify-the-cpp-rules-to-run.md)
- [Kod analizi araçlarını kullanarak sürücü kalitesini analiz etme](/windows-hardware/drivers/develop/analyzing-driver-quality-by-using-code-analysis-tools)
- [Sürücüler için kod analizi uyarıları](/windows-hardware/drivers/devtest/prefast-for-drivers-warnings)
