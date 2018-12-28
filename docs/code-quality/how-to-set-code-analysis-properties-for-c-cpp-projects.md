---
title: 'Nasıl Yapılır: C/C++ projeleri için Kod Analizi özelliklerini ayarlama'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.propertypages.native
- VC.Project.VCCLCompilerTool.EnablePrefast
- VC.Project.VCFxCopTool.EnablePREfast
- VC.Project.VCFxCopTool.IgnoreGeneratedCode
helpviewer_keywords:
- properties, C/C++ Code Analysis
- properties, Code Analysis
- code analysis properties
- C/C++ code analysis properties
ms.assetid: 7af52097-6d44-4785-9b9f-43b7a7d447d7
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- cplusplus
ms.openlocfilehash: a9de737604da898c42243895ed84e8962a8c656f
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53803158"
---
# <a name="how-to-set-code-analysis-properties-for-cc-projects"></a>Nasıl Yapılır: C/C++ projeleri için Kod Analizi özelliklerini ayarlama
Kod çözümleme aracı her projenizin yapılandırmasını kodda çözümlemek için hangi kuralları kullanacağını yapılandırabilirsiniz. Ayrıca, oluşturulan ve projenize bir üçüncü taraf araç tarafından eklenen koddan uyarıları bastırmak için Kod Analizi yönlendirebilir.

## <a name="code-analysis-property-page"></a>Kod Analizi özellik sayfası
 **Kod Analizi** özellik sayfası, proje için tüm kod analizi yapılandırma ayarlarını içerir. Bir proje için Kod Analizi özellik sayfasını açmak için **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **özellikleri**. Ardından, genişletme **yapılandırma özellikleri** seçip **Kod Analizi** sekmesi.

## <a name="project-configuration-and-platform"></a>Proje yapılandırması ve platformu
 **Yapılandırma** listesi ve **Platform** listesi farklı proje yapılandırma ve platform bileşimleri için farklı kod analizi ayarları uygulamanıza olanak tanır. Örneğin, projeniz için hata ayıklama için bir kural kümesi uygulamak için Kod Analizi yapıları ve sürüm için farklı bir küme oluşturur yönlendirebilir.

## <a name="enabling-code-analysis"></a>Kod analizini etkinleştirme
 Projeniz için Kod Analizi seçerek etkinleştirip etkinleştirmemeye karar **etkinleştirmek Kod Analizi C/C++ için derleme üzerinde**. İle birlikte **yapılandırma** listesi Örneğin, karar hata ayıklama yapıları ve etkinleştirmek için sürüm derlemeleri için Kod Analizi devre dışı bırakmak.

 Yönetilen Kod projenizi içeren, etkinleştirme veya Kod Analizi seçerek devre dışı karar verebilir **derlemede kod analizini etkinleştir**.

 Kod Analizi, kodunuzun kalitesini ve yaygın görülen tehlikeleri önlemek amacıyla tasarlanmıştır. Bu nedenle, dikkatlice Kod Analizi devre dışı bırakılıp bırakılmayacağını. Kural kümeleri devre dışı bırakmak daha iyi veya projenize istemediğiniz bireysel kuralları uygulanır.

## <a name="generated-code"></a>Oluşturulan kod
 Geliştiriciler, uygulamaları hızla geliştirmenizi sağlayacak sık araçlarını kullanın. Bu araçlar, projeye eklenen kod oluşturabilirsiniz. Kod Analizi üretilen kodda bulur kural ihlalleri görmek isteyebilirsiniz. Ancak, kodunu korumak istemiyorsanız görmek istemeyebilirsiniz.

 **Bastır sonuçları oluşturulan kodun** onay kutusunu **genel** özellikleri sayfasında, bir üçüncü taraf araç tarafından oluşturulan yönetilen koddan kod çözümleme uyarıları görmek istediğiniz istemediğinizi sağlar .

## <a name="rule-sets"></a>Kural Kümeleri
 Yönetilen Kod projenizi içeren, bir kural kümesini seçerek bir kod analizi uygulanacak kuralları seçebilirsiniz **bu kural kümesini Çalıştır** listesi.

## <a name="see-also"></a>Ayrıca Bkz.

- [Yönetilen Kod Kalitesini Analiz Etme](../code-quality/code-analysis-for-managed-code-overview.md)
- [C/C++ İçin Kod Analizi Uyarıları](../code-quality/code-analysis-for-c-cpp-warnings.md)