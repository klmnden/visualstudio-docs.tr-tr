---
title: Standart Kod Analizi İade İlkeleri Oluşturma veya Güncelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.policyeditor
helpviewer_keywords:
- code analysis, migrating check-in policy
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 768efb3e874f6427cd23f63f14671aa2db1bea71
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55917083"
---
# <a name="how-to-create-or-update-standard-code-analysis-check-in-policies"></a>Nasıl yapılır: Standart Kod Analizi İade İlkeleri Oluşturma veya Güncelleştirme

Kod çözümleme İade İlkesi'ni kullanarak kod analizi tüm kod projesinde bir Azure DevOps projesi üzerinde çalıştırılması gerektirebilir. Kod Analizi gerektiren kod tabanında denetlenen kodun kalitesini artırabilir.

> [!NOTE]
> Bu özellik yalnızca Team Foundation Server kullanıyorsanız kullanılabilir.

Kod çözümleme iade ilkeleri proje ayarlarında belirlenir ve her kod projesi için geçerli. Kod Analizi yürütmeleri kod projesi için proje (.xxproj) dosyasında kod projeleri için yapılandırılır. Kod Analizi yürütmeleri yerel bilgisayarda gerçekleştirilir. Proje ayarlarını kurallarında çevrili Kod Analizi ilkesini etkinleştirmek, son kullanıcıların düzenlemeden sonra iade edilmesi için bir kod projesi dosyalarda derlenmiş ve en az bir kod analizini çalıştırdığınızda, içeren bilgisayarda gerçekleştirilmelidir burada Değiştir s yapıldı.

- Yönetilen kod için iade ilkesi belirterek ayarladığınız bir *kural kümesi* , bir alt kod analizi kuralları içerir.

- Visual Studio 2017 sürüm 15.6 ve önceki sürümlerde, C/C++ kodu için tüm kod analizi kuralları çalıştırılır iade ilkesi gerektirir. Ön İşlemci yönergeleri, Azure DevOps projesi bireysel kod projeleri için belirli kuralları devre dışı bırakmak için ekleyebilirsiniz. 15.7 ve daha sonra kullanabileceğiniz **/ analyze: ruleset** çalıştırmak için hangi kuralları belirtmek için. Daha fazla bilgi için [çalıştırılacak C++ kurallarını belirtmek için kural kümeleri kullanma](using-rule-sets-to-specify-the-cpp-rules-to-run.md).

İade İlkesi yönetilen kod için belirttikten sonra ekip üyeleri kendi Azure DevOps projesi ilke ayarlarında kod projeleri için Kod Analizi ayarları eşitleyebilirsiniz.

## <a name="to-open-the-check-in-policy-editor"></a>İade İlkesi Düzenleyicisi'ni açmak için

1. Takım Gezgini'nde proje adına sağ tıklayın, fareyle **proje ayarları**ve ardından **kaynak denetimi**.

1. İçinde **kaynak denetimi** iletişim kutusunda **iade ilkesi** sekmesi.

1. Aşağıdakilerden birini yapın:

    - Tıklayın **Ekle** yeni bir iade ilkesi oluşturulacak.

    - Var olan çift **Kod Analizi** öğesi **ilke türü** ilkeyi değiştirmek için liste.

## <a name="to-set-policy-options"></a>İlke seçeneklerini ayarlamak için

Seçin veya aşağıdaki seçenekleri temizleyin:

|Seçenek|Açıklama|
|------------|-----------------|
|**Yalnızca geçerli çözümün bir parçası olan dosyaları içerecek şekilde iade uygular.**|Kod Analizi, çözüm ve proje yapılandırma dosyalarında belirtilen dosyalar üzerinde çalıştırabilirsiniz. Bu ilke, bir çözümün parçası olan tüm kod analiz edilen garanti eder.|
|**C/C++ kod analizini zorla (/ analyze)**|Tüm C veya C++ projeleri ile oluşturulması gerekir / analyze derleyici seçeneği, Kod Analizi iade edilmeden önce çalıştırılacak.|
|**Yönetilen kod için kod analizini zorla**|Tüm yönetilen projeleri için kod analizini Çalıştır ve iade edilmeden önce yapı gerektirir.|

## <a name="to-specify-a-managed-rule-set"></a>Bir yönetilen kural kümesi belirtmek için

Gelen **bu kural kümesini Çalıştır** listesinde, aşağıdaki yöntemlerden birini kullanın:

- Bir Microsoft Standart kural kümesi seçin.

- Tıklayarak özel bir kural seçin  **\<kaynak denetiminden kural kümesi seçin >**. Ardından, kural kümesi kaynak denetimi tarayıcıda sürüm denetim yolunu yazın. Bir sürüm denetim yolu sözdizimi aşağıdaki gibidir:

   **$/** `TeamProjectName` **/** `VersionControlPath`

Oluşturma ve bir özel iade ilkesi kuralı uygulamak hakkında daha fazla bilgi için bkz: [yönetilen kod için uygulayan özel iade ilkeleri](../code-quality/implementing-custom-code-analysis-check-in-policies-for-managed-code.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Oluşturma ve kod çözümleme iade ilkelerini kullanma](../code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies.md)