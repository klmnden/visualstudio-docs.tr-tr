---
title: Bir çözümde birden çok DSL | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 7e668620-6217-4e87-aea7-e9036776c8e4
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d70794dddc02605c76c1af330a49af4be917c0e3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68159007"
---
# <a name="multiple-dsls-in-one-solution"></a>Bir Çözümde Birden Çok DSL
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bunlar birlikte yüklenir, böylece tek bir çözümün bir parçası birkaç DSL'ler paketleyebilirsiniz.  
  
 Birden çok DSL tümleştirmek için çeşitli teknikler kullanabilirsiniz. Daha fazla bilgi için [Visual Studio Modelbus kullanarak modelleri tümleştirme](../modeling/integrating-models-by-using-visual-studio-modelbus.md) ve [nasıl yapılır: Bir Sürükle ve bırak işleyicisi ekleme](../modeling/how-to-add-a-drag-and-drop-handler.md) ve [kopyalama davranışını özelleştirme](../modeling/customizing-copy-behavior.md).  
  
### <a name="to-build-more-than-one-dsl-in-the-same-solution"></a>Aynı çözümdeki birden çok DSL oluşturmak için  
  
1. İki veya daha fazla DSL çözümler ve bir VSIX projesi oluşturun ve tüm projeler tek bir çözüme ekleyin.  
  
   - Yeni bir VSIX projesi oluşturmak için: İçinde **yeni proje** iletişim kutusunda **Visual C#** , **genişletilebilirlik**, **VSIX projesi**.  
  
   - VSIX çözüm dizininde değil iki veya daha fazla DSL çözümleri oluşturun.  
  
        Her bir DSL için Visual Studio'nun yeni bir örneğini açın. Yeni DSL oluşturun ve VSIX çözümle aynı çözüm klasörü belirtin.  
  
        Farklı bir dosya adı uzantısı ile her DSL oluşturduğunuzdan emin olun.  
  
   - Adlarını değiştirme **Dsl** ve **DslPackage** böylece tüm farklıdır projeleri. Örneğin: `Dsl1`, `DslPackage1`, `Dsl2`, `DslPackage2`.  
  
   - Her **DslPackage\*\source.extension.tt**, bu satırı doğru Dsl projesi adıyla güncelleştirin:  
  
        `string dslProjectName = "Dsl2";`  
  
   - Dsl * ve DslPackage VSIX çözümüne ekleme\* projeleri.  
  
        Kendi çözüm klasöründe her çifti yerleştirmek isteyebilirsiniz.  
  
2. DSL VSIX bildirimlerini Birleştir:  
  
   1. Açık _YourVsixProject_ **\source.extension.manifest**.  
  
   2. Her bir DSL seçin **İçerik Ekle** ekleyin:  
  
       - `Dsl*` Proje olarak bir **MEF Bileşeni**  
  
       - `DslPackage*` Proje olarak bir **MEF Bileşeni**  
  
       - `DslPackage*` Proje olarak bir **VS paket**  
  
3. Çözümü oluşturun.  
  
   Sonuçta elde edilen VSIX hem DSL'ler yükler. F5 kullanarak test edebilir veya dağıtma _YourVsixProject_ **\bin\Debug\\\*.vsix**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Modelbus kullanarak modelleri tümleştirme](../modeling/integrating-models-by-using-visual-studio-modelbus.md)   
 [Nasıl yapılır: Bir Sürükle ve bırak işleyicisi ekleme](../modeling/how-to-add-a-drag-and-drop-handler.md)   
 [Kopyalama Davranışını Özelleştirme](../modeling/customizing-copy-behavior.md)
