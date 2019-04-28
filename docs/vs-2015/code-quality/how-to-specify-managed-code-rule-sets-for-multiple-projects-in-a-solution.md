---
title: 'Nasıl yapılır: Bir çözümde birden çok proje için yönetilen kod kural kümesi belirtme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.propertypages.solution
ms.assetid: 92dc3250-a010-4396-b515-f03a0b30cd2a
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 555f8cb0ace4386a3fba7730980295dc16e58b2a
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63426666"
---
# <a name="how-to-specify-managed-code-rule-sets-for-multiple-projects-in-a-solution"></a>Nasıl yapılır: Bir çözümde birden çok proje için yönetilen kod kural kümesi belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, Microsoft en az önerilen kurallar Kod Analizi bir çözümün tüm yönetilen projelere atanır *kural kümesi*. Proje Özellikleri iletişim kutusunda çözüm için bir çözüm atanmış olan kural kümeleri değiştirebilirsiniz.  
  
> [!NOTE]
> Varsayılan olarak, Kod Analizi projesi bir derleme adımı olarak çalıştırılmaz. Kod Analizi bir derleme adımı olarak etkinleştirmek için bkz: [nasıl yapılır: Yönetilen kod projesi için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md).  
  
### <a name="to-specify-a-rule-set-for-multiple-projects-in-a-managed-code--solution"></a>Yönetilen kod çözümde birden çok proje için bir kural belirtmek için  
  
1. İçinde [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)]. [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], veya [!INCLUDE[vsPro](../includes/vspro-md.md)] çözümü açın.  
  
2. Üzerinde **Çözümle** menüsünde tıklatın **çözüm için Kod Analizi yapılandırma**.  
  
3. Gerekirse genişletin **ortak özellikler**ve ardından **Kod Analizi ayarları**.  
  
4. Bir veya daha fazla proje için bir kural belirtebilirsiniz.  
  
    - Bir kural kümesi için bir projeyi belirtmek için proje adına tıklayın.  
  
    - Birden çok proje için bir kural belirtmek için CTRL tuşunu basılı tutun ve proje adları tıklayın.  
  
    - Çözümdeki tüm projeleri belirtmek için SHIFT tuşunu basılı tutun ve Proje listesinde tıklayın.  
  
5. Tıklayın **kural kümesi** alan bir proje ve kural adını ayarlayın uygulamak istediğiniz'a tıklayın.
