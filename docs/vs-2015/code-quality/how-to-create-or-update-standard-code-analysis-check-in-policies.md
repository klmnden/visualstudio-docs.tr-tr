---
title: 'Nasıl yapılır: Oluşturma veya güncelleştirme standart kod çözümleme iade ilkeleri | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.policyeditor
helpviewer_keywords:
- code analysis, migrating check-in policy
ms.assetid: 458eb3b8-bb5e-4056-82b7-7079ce9c4089
caps.latest.revision: 31
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: caaf9026d949b2e1327e7d88507f27392bf07283
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54834016"
---
# <a name="how-to-create-or-update-standard-code-analysis-check-in-policies"></a>Nasıl yapılır: Standart Kod Analizi İade İlkeleri Oluşturma veya Güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kod çözümleme İade İlkesi'ni kullanarak kod analizi bir takım projesindeki tüm kod projeleri üzerinde çalıştırılması gerektirebilir. Kod Analizi gerektiren kod tabanında denetlenen kodun kalitesini artırabilir.  
  
> [!NOTE]
>  Bu özellik yalnızca Team Foundation Server kullanıyorsanız kullanılabilir.  
  
 Kod çözümleme iade ilkeleri, takım proje ayarlarında belirlenir ve her kod projesini takım projesinde geçerli. Kod Analizi yürütmeleri kod projesi için proje (.xxproj) dosyasında kod projeleri için yapılandırılır. Kod Analizi yürütmeleri yerel bilgisayarda gerçekleştirilir. İade Kod Analizi ilkesini etkinleştirmek, son kullanıcıların düzenlemeden sonra iade edilmesi için bir kod projesi dosyalarda derlenmiş ve en az bir kod analizini çalıştırdığınızda, içeren takım projesi ayarlarını kurallarında bilgisayarda gerçekleştirilmesi gereken yere c değişiklikleri yapıldı.  
  
- Yönetilen kod için iade ilkesi belirterek ayarladığınız bir *kural kümesi* , bir alt kod analizi kuralları içerir.  
  
- C/C++ kodu için tüm kod analizi kuralları çalıştırılır iade ilkesi gerektirir. Takım projenizdeki bireysel kod projeleri için belirli kuralları devre dışı bırakmak için ön işlemci yönergeleri ekleyebilirsiniz.  
  
  İade İlkesi yönetilen kod için belirttikten sonra takım üyeleri, takım projesi ilke ayarları için kod projeleri için Kod Analizi ayarları eşitleyebilirsiniz.  
  
### <a name="to-open-the-check-in-policy-editor"></a>İade İlkesi Düzenleyicisi'ni açmak için  
  
1.  Takım projesi adı Ekip Gezgini'nde sağ tıklatın, **takım projesi ayarları**ve ardından **kaynak denetimi**.  
  
2.  İçinde **kaynak denetimi** iletişim kutusunda **iade ilkesi** sekmesi.  
  
3.  Aşağıdakilerden birini yapın:  
  
    -   Tıklayın **Ekle** yeni bir iade ilkesi oluşturulacak.  
  
    -   Var olan çift **Kod Analizi** öğesi **ilke türü** ilkeyi değiştirmek için liste.  
  
### <a name="to-set-policy-options"></a>İlke seçeneklerini ayarlamak için  
  
-   Seçin veya aşağıdaki seçenekleri temizleyin:  
  
    |Seçenek|Açıklama|  
    |------------|-----------------|  
    |**Yalnızca geçerli çözümün bir parçası olan dosyaları içerecek şekilde iade uygular.**|Kod Analizi, çözüm ve proje yapılandırma dosyalarında belirtilen dosyalar üzerinde çalıştırabilirsiniz. Bu ilke, bir çözümün parçası olan tüm kod analiz edilen garanti eder.|  
    |**C/C++ kod analizini zorla (/ analyze)**|Tüm C veya C++ projeleri ile oluşturulması gerekir / analyze derleyici seçeneği, Kod Analizi iade edilmeden önce çalıştırılacak.|  
    |**Yönetilen kod için kod analizini zorla**|Tüm yönetilen projeleri için kod analizini Çalıştır ve iade edilmeden önce yapı gerektirir.|  
  
-  
  
### <a name="to-specify-a-managed-rule-set"></a>Bir yönetilen kural kümesi belirtmek için  
  
-   Gelen **bu kural kümesini Çalıştır** listesinde, aşağıdaki yöntemlerden birini kullanın:  
  
    -   Bir Microsoft Standart kural kümesi seçin.  
  
    -   Özel kural kümesi seçmek için tıklatın  **\<kaynak denetiminden kural kümesi seçin >**, kural kümesi kaynak denetimi tarayıcıda sürüm denetim yolunu yazın. Bir sürüm denetim yolu sözdizimi aşağıdaki gibidir:  
  
    -   **$/** `TeamProjectName` **/** `VersionControlPath`  
  
    -   Oluşturma ve bir özel iade ilkesi kuralı uygulamak hakkında daha fazla bilgi için bkz: [yönetilen kod için uygulamaya özel iade ilkeleri](../code-quality/implementing-custom-code-analysis-check-in-policies-for-managed-code.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kod Çözümleme İade İlkeleri Oluşturma ve Kullanma](../code-quality/creating-and-using-code-analysis-check-in-policies.md)
