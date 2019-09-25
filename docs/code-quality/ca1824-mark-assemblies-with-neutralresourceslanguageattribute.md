---
title: 'CA1824: Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin'
ms.date: 03/29/2018
ms.topic: reference
f1_keywords:
- CA1824
- MarkAssembliesWithNeutralResourcesLanguage
helpviewer_keywords:
- MarkAssembliesWithNeutralResourcesLanguage
- CA1824
ms.assetid: 10e97f8a-aa6e-47aa-b253-1e5d3a295d82
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: df5c0db4e9e141e5833893bbbb447328eab8851e
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233352"
---
# <a name="ca1824-mark-assemblies-with-neutralresourceslanguageattribute"></a>CA1824: Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkAssembliesWithNeutralResourcesLanguage|
|CheckId|CA1824|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir derleme, <xref:System.Resources.NeutralResourcesLanguageAttribute?displayProperty=fullName> **resx**tabanlı bir kaynak içerir ancak ona uygulanmaz.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Resources.NeutralResourcesLanguageAttribute> Özniteliği, bir uygulamanın varsayılan kültürünün kaynak yöneticisini bilgilendirir. Varsayılan kültürün kaynakları uygulamanın ana derlemesine katıştırılmışsa ve <xref:System.Resources.ResourceManager> varsayılan kültür <xref:System.Resources.ResourceManager> ile aynı kültüre ait olan kaynakları alması gerekiyorsa, ana derlemede bulunan kaynakları otomatik olarak kullanır bir uydu derlemesi aramak yerine. Bu, olağan derleme araştırmasını atlar, yüklediğiniz ilk kaynak için arama performansını geliştirir ve çalışma kümesini azaltabilir.

> [!TIP]
> Bkz. kaynak dosyalarını araştırmada <xref:System.Resources.ResourceManager> kullanılan işlem için [kaynakları paketleme ve dağıtma](/dotnet/framework/resources/packaging-and-deploying-resources-in-desktop-apps) .

## <a name="fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, derlemeye özniteliği ekleyin ve nötr kültürün kaynak dilini belirtin.

### <a name="to-specify-the-neutral-language-for-resources"></a>Kaynakların bağımsız dilini belirtmek için

1. **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **Özellikler**' i seçin.

2. **Uygulama** sekmesini seçin ve ardından **derleme bilgileri**' ni seçin.

   > [!NOTE]
   > Projeniz bir .NET Standard veya .NET Core projesi ise, **paket** sekmesini seçin.

3. **Nötr dil** veya **bütünleştirilmiş kod nötr dili** açılan listesinden dili seçin.

4. **Tamam**’ı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarı gösterilmemek için izin verilir. Ancak, başlangıç performansı düşebilir.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Resources.NeutralResourcesLanguageAttribute>
- [Masaüstü uygulamalarındaki kaynaklar (.NET)](/dotnet/framework/resources/)
- [CA1703-kaynak dizeleri doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)
- [CA1701-kaynak dizesi bileşik sözcüklerin doğru şekilde kullanılması gerekir](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)