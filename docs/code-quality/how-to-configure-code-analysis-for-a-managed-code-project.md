---
title: Kod analizini yapılandırma
ms.date: 04/04/2018
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.propertypages.csvb
- vs.codeanalysis.propertypages.solution
helpviewer_keywords:
- code analysis, selecting rule sets
- code analysis, rule sets
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: f3c8fbde60e247ca9ec5fe82c9a16f28aded2abc
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66715052"
---
# <a name="how-to-configure-static-code-analysis-for-managed-code"></a>Nasıl yapılır: Yönetilen kod için statik kod analizini yapılandırma

Visual Studio'da Kod Analizi listesinden seçebilirsiniz [kural kümeleri](../code-quality/rule-set-reference.md) yönetilen kod projesi için uygulanacak. Varsayılan olarak, **Microsoft en az önerilen kurallar** kural kümesi işaretli, ancak isterseniz kümesi farklı bir kural uygulayabilirsiniz. Bir çözümde bir veya birden çok proje için kural kümeleri uygulanabilir.

ASP.NET web uygulamaları için bir kural yapılandırma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Bir ASP.NET web uygulaması için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md).

> [!NOTE]
> Bu makalede, statik kod analizi ve değil geçerlidir [Roslyn Çözümleyicileri](use-roslyn-analyzers.md), derlemeden sonra kod analizi çalıştırılması yok.

## <a name="configure-a-rule-set-for-a-net-framework-project"></a>Bir kural kümesi için bir .NET Framework projesinin yapılandırma

1. Açık **Kod Analizi** projenin özellik sayfalarındaki sekmesinde. Bu aşağıdaki yollardan biriyle yapabilirsiniz:

   - İçinde **Çözüm Gezgini**, projeyi seçin. Menü çubuğunda, seçin **Çözümle** > **Kod Analizi yapılandırma** > **için \<projectname >** .

   - Projeye sağ **Çözüm Gezgini** seçip **özellikleri**ve ardından **Kod Analizi** sekmesi.

1. İçinde **yapılandırma** ve **Platform** listeleri, derleme yapılandırması ve hedef platformu seçin.

1. Seçili yapılandırma kullanarak proje oluşturulan her zaman, Kod Analizi çalıştırmak için seçin **derlemede kod analizini etkinleştir** onay kutusu. Ayrıca kod analizini el ile seçerek çalıştırabilirsiniz **Çözümle** > **kod çözümlemeyi Çalıştır** > **kod çözümlemeyi Çalıştır \<projectname >** .

1. Varsayılan olarak, Kod Analizi uyarıları otomatik olarak dış araçları tarafından oluşturulan kodu raporlamaz. Üretilen koddan gelen uyarıları görüntülemek için temizleyin **üretilen koddan gelen sonuçları Gizle** onay kutusu.

    > [!NOTE]
    > Bu seçenek hataları ve Uyarıları formları ve şablonlar görüntülendiğinde kod çözümleme hataları ve Uyarıları üretilen koddan gelen engellemez. Hem görüntüleyebilir ve bir form veya şablon için kaynak kodu, üzerine zorunda kalmadan korumak.

1. İçinde **bu kural kümesini Çalıştır** listesinde, aşağıdakilerden birini yapın:

    - Kullanmak istediğiniz bir kural kümesi seçin.

    - Seçin  **\<Gözat … >** var olan bir özel kural kümesi bulmak için listesinde değil.

    - Tanımlayan bir [özel kural kümesi](../code-quality/how-to-create-a-custom-rule-set.md).

## <a name="specify-rule-sets-for-multiple-projects-in-a-solution"></a>Bir çözümde birden çok proje için kural kümeleri belirtin

Varsayılan olarak, bir çözümün tüm yönetilen projelere atanır *Microsoft en az önerilen kurallar* Kod Analizi kural kümesi. Bir Çözümdeki projeler için atanan kural kümeleri değiştirebilirsiniz **özellikleri** çözümü iletişim kutusu.

1. Visual Studio içinde çözümü açın.

2. Üzerinde **Çözümle** menüsünde **çözüm için Kod Analizi yapılandırma**.

3. Gerekirse genişletin **ortak özellikler**ve ardından **Kod Analizi ayarları**.

4. Bir veya daha fazla proje için bir kural belirtebilirsiniz:

    - Bir kural kümesi için bir projeyi belirtmek için proje adını seçin.

    - Birden çok proje için bir kural belirtmek için basılı **Ctrl** ve proje adları seçin.

    - Çözümdeki tüm projeleri belirtmek için basılı **Shift** ve Proje listesinde tıklayın.

5. Seçin **kural kümesi** bir proje alanı ve ardından uygulamak istediğiniz kuralın adını ayarlayın.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod çözümleme kural kümesi başvurusu](../code-quality/rule-set-reference.md)
- [Nasıl yapılır: Bir ASP.NET web uygulaması için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md)
