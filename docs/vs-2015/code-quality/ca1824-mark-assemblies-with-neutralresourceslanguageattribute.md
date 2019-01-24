---
title: 'CA1824: Derlemeleri NeutralResourcesLanguageAttribute ile işaretleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1824
- MarkAssembliesWithNeutralResourcesLanguage
helpviewer_keywords:
- MarkAssembliesWithNeutralResourcesLanguage
- CA1824
ms.assetid: 10e97f8a-aa6e-47aa-b253-1e5d3a295d82
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 8690a1f05f54fbac9427f4a03412e0a8054c51d2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779921"
---
# <a name="ca1824-mark-assemblies-with-neutralresourceslanguageattribute"></a>CA1824: Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkAssembliesWithNeutralResourcesLanguage|
|CheckId|CA1824|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir derlemeyi içeren bir **ResX**-yoktur ancak kaynak tabanlı <xref:System.Resources.NeutralResourcesLanguageAttribute?displayProperty=fullName> uygulanmış.

## <a name="rule-description"></a>Kural Tanımı
 **NeutralResourcesLanguage** öznitelik bildirir **ResourceManager** bir derleme için nötr kültürün kaynakları görüntülemek için kullanılan dili. Bağımsız kaynaklar dili ile aynı kültüründeki kaynakları göründüğünde **ResourceManager** otomatik olarak ana derlemede bulunan kaynakları kullanır. Geçerli iş parçacığı için geçerli kullanıcı arabirimi kültürünü sahip bir uydu derleme aramak yerine bunu yapar. Bu ilk yüklediğiniz kaynak için arama performansını artırır ve çalışma kümenizi azaltabilir.

## <a name="fixing-violations"></a>İhlalleri düzeltme
 Bu kural ihlalini düzeltmek için özniteliği derlemeye ekleyin ve dil nötr kültürün kaynakları belirtin.

## <a name="specifying-the-language"></a>Dil belirtme

#### <a name="to-specify-the-language-of-the-resource-of-the-neutral-culture"></a>Nötr kültürün kaynağın dilini belirtmek için

1.  İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri**.

2.  Sol gezinti çubuğundan seçin **uygulama**ve ardından **derleme bilgileri**.

3.  İçinde **derleme bilgileri** iletişim kutusunda, dili seçin **nötr dil** aşağı açılan listesi.

4.  **Tamam**'ı tıklatın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak için izin verilebilir. Ancak, başlangıç performansı düşürebilir.
