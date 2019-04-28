---
title: Seçenekler, metin düzenleyici, JavaScript, proje
ms.date: 1/15/2019
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Project.General
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Project
- VS.ToolsOptionsPages.Text_Editor.TypeScript.Project.General
- VS.ToolsOptionsPages.Text_Editor.TypeScript.Project
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 09ed64d6bffaa4453c3294229ee48fd0a065eb74
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62778179"
---
# <a name="options-text-editor-javascript-project"></a>Seçenekler, metin düzenleyici, JavaScript, proje

Kullanım **proje** sayfasının **seçenekleri** iletişim kutusu Kod Düzenleyicisi'nde JavaScript proje seçenekleri belirtin. Menü çubuğunda, bu sayfaya erişmek için seçin **Araçları** > **seçenekleri**ve ardından **metin düzenleyici** > **JavaScript**  >  **Proje**.

## <a name="project-analysis-options"></a>Proje Analizi seçenekleri

Bu seçenekler nasıl Düzenleyicisi projeleri analiz eder, tanılama raporları ve iyileştirmeleri önerir belirler. Seçin veya düzenleyici bunlardan nasıl işleyeceğini belirtmek için bu seçenekleri temizleyin.

### <a name="uielement-list"></a>UIElement listesi

- **Yalnızca düzenleyicide açılan dosyalar içeren projeleri analiz et**
- **Yalnızca düzenleyicide açılan dosyalar için tanılamaları raporla**
- **Düzeltmeleri olmayan olası geliştirmeleri önerin**

## <a name="virtual-projects-in-solution-explorer"></a>Çözüm Gezgini'ndeki sanal projeler

Bu seçenekler bir çözüm olduğunda sanal projeleri görüntülemek için yüklenmiş veya yüklü olup olmadığını seçmenize izin verir.

## <a name="compile-on-save"></a>Derleme ile tasarruf

Bu seçenekler, projenin parçası olmayan bir TypeScript dosyalarını otomatik olarak derlenmiş olup olmadığını belirler. Onay kutusunu işaretleyin ve ardından kullanmak için kod oluşturma türünü seçin.

### <a name="uielement-list"></a>UIElement listesi

- **Bir projenin parçası olmayan modüller için AMD kod üretimini kullan**
- **Bir projenin parçası olmayan modüller için CommonJS kod üretimini kullan**
- **Bir projenin parçası olmayan modüller için UMD kod üretimini kullan**
- **Bir projenin parçası olmayan modüller için sistem kod üretimini kullan**
- **Bir projenin parçası olmayan modüller için ES2015 kod üretimini kullan**

## <a name="ecmascript-version-for-files-that-are-not-part-of-a-project"></a>Bir projenin parçası olmayan dosyalar için ECMAScript sürümü

Bu seçenekler, bir projenin parçası olmayan dosyalar için ECMAScript sürümü seçmenize olanak tanır. Arasından seçim yapabilirsiniz **ECMAScript 3**, **ECMAScript 5**, veya **ECMAScript 6**.

## <a name="jsx-emit-for-tsx-files-that-are-not-part-of-a-project"></a>Bir projenin parçası olmayan TSX dosyaları için JSX yayma

Bu seçenekler, Düzenleyici bir projenin parçası olmayan bir TypeScript dosyaları nasıl işler belirler.

### <a name="uielement-list"></a>UIElement listesi

|Seçenek|Açıklama|
|------------|-----------------|
|**React Framework**|Bu seçenek belirlendiğinde, Kod Düzenleyicisi yayan bir *.js* dosya uzantısı.|
|**Koru**|Bu seçenek belirlendiğinde, Kod Düzenleyicisi çıkış bir parçası olarak JSX tutar ve yayan bir *.jsx* dosya uzantısı.|

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)