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
ms.openlocfilehash: 40cb2a3674884a9fb4f1449c9afa2e0a2d27050f
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55919150"
---
# <a name="ca1824-mark-assemblies-with-neutralresourceslanguageattribute"></a>CA1824: Derlemeleri NeutralResourcesLanguageAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkAssembliesWithNeutralResourcesLanguage|
|CheckId|CA1824|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir derlemeyi içeren bir **ResX**-yoktur ancak kaynak tabanlı <xref:System.Resources.NeutralResourcesLanguageAttribute?displayProperty=fullName> uygulanmış.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Resources.NeutralResourcesLanguageAttribute> Öznitelik, bir uygulamanın varsayılan kültürünün kaynak yöneticisi bildirir. Varsayılan kültürün kaynakları uygulamanın ana derlemede gömülü değilse ve <xref:System.Resources.ResourceManager> varsayılan kültürüyle aynı kültürü ait kaynakları almak sahip <xref:System.Resources.ResourceManager> otomatik olarak ana derlemede bulunan kaynakları kullanır. için bir uydu derleme aramak yerine. Bu, normal derleme araştırma atlar, yükleme ve çalışma kümenizi azaltabilir ilk kaynağın Arama performansını artırır.

> [!TIP]
> Bkz: [paketleme ve dağıtma kaynakları](/dotnet/framework/resources/packaging-and-deploying-resources-in-desktop-apps) işlem için <xref:System.Resources.ResourceManager> kaynak dosyaları için araştırma için kullanır.

## <a name="fix-violations"></a>İhlallerini düzeltmek

Bu kural ihlalini düzeltmek için özniteliği derlemeye ekleyin ve dil nötr kültürün kaynakları belirtin.

### <a name="to-specify-the-neutral-language-for-resources"></a>Nötr dil kaynakları belirtmek için

1. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri**.

2. Seçin **uygulama** sekmesine tıklayın ve ardından **derleme bilgileri**.

   > [!NOTE]
   > Projeniz .NET Standard veya .NET Core projesiyse seçin **paket** sekmesi.

3. Dili seçin **dilden** veya **derleme dilden** aşağı açılan listesi.

4. **Tamam**’ı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı bastırmak için izin verilebilir. Ancak, başlangıç performansı düşebilir.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Resources.NeutralResourcesLanguageAttribute>
- [(.NET) Masaüstü uygulamalarındaki kaynaklar](/dotnet/framework/resources/)
- [CA1703 - kaynak dizeler doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)
- [CA1701 - kaynak dizesi bileşik sözcüklerin doğru yazılmalıdır](../code-quality/ca1701-resource-string-compound-words-should-be-cased-correctly.md)