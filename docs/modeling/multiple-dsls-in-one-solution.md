---
title: Bir Çözümde Birden Çok DSL
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 87d9e4ae8239994a7524cdd1da0b3cfe05ea42d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62808190"
---
# <a name="multiple-dsls-in-one-solution"></a>Bir Çözümde Birden Çok DSL

Bunlar birlikte yüklenir, böylece tek bir çözümün bir parçası birkaç DSL'ler paketleyebilirsiniz.

Birden çok DSL tümleştirmek için çeşitli teknikler kullanabilirsiniz. Daha fazla bilgi için [Visual Studio Modelbus kullanarak modelleri tümleştirme](../modeling/integrating-models-by-using-visual-studio-modelbus.md) ve [nasıl yapılır: Bir Sürükle ve bırak işleyicisi ekleme](../modeling/how-to-add-a-drag-and-drop-handler.md) ve [kopyalama davranışını özelleştirme](../modeling/customizing-copy-behavior.md).

## <a name="build-more-than-one-dsl-in-the-same-solution"></a>Aynı çözümdeki birden çok DSL oluşturun

1. Yeni bir **VSIX projesi** proje.

2. VSIX çözüm dizininde değil iki veya daha fazla DSL projesi oluşturun.

   - Her bir DSL için Visual Studio'nun yeni bir örneğini açın. Yeni DSL oluşturun ve VSIX çözümle aynı çözüm klasörü belirtin.

   - Farklı bir dosya adı uzantısı ile her DSL oluşturduğunuzdan emin olun.

   - Adlarını değiştirme **Dsl** ve **DslPackage** böylece tüm farklıdır projeleri. Örneğin: `Dsl1`, `DslPackage1`, `Dsl2`, `DslPackage2`.

   - Her **DslPackage\*\source.extension.tt**, bu satırı doğru Dsl projesi adıyla güncelleştirin:

      `string dslProjectName = "Dsl2";`

   - Dsl * ve DslPackage VSIX çözümüne ekleme\* projeleri. Kendi çözüm klasöründe her çifti yerleştirmek isteyebilirsiniz.

2. DSL VSIX bildirimlerini Birleştir:

   1. Açık _YourVsixProject_**\source.extension.manifest**.

   2. Her bir DSL seçin **İçerik Ekle** ekleyin:

       - `Dsl*` Proje olarak bir **MEF Bileşeni**

       - `DslPackage*` Proje olarak bir **MEF Bileşeni**

       - `DslPackage*` Proje olarak bir **VS paket**

3. Çözümü oluşturun.

   Sonuçta elde edilen VSIX hem DSL'ler yükler. F5 kullanarak test edebilir veya dağıtma _YourVsixProject_**\bin\Debug\\\*.vsix**.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio Modelbus'ı Kullanarak Modelleri Tümleştirme](../modeling/integrating-models-by-using-visual-studio-modelbus.md)
- [Nasıl yapılır: Sürükle ve Bırak İşleyicisi Ekleme](../modeling/how-to-add-a-drag-and-drop-handler.md)
- [Kopyalama Davranışını Özelleştirme](../modeling/customizing-copy-behavior.md)