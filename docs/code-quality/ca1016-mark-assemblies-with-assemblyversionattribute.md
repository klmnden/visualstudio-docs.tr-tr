---
title: 'CA1016: Derlemeleri AssemblyVersionAttribute ile işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MarkAssembliesWithAssemblyVersion
- CA1016
helpviewer_keywords:
- CA1016
- MarkAssembliesWithAssemblyVersion
ms.assetid: 4340aed8-d92b-4cde-a398-cb6963c6da5a
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: a00c8e30e981794e69d4572e0a924438514780c7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779576"
---
# <a name="ca1016-mark-assemblies-with-assemblyversionattribute"></a>CA1016: Derlemeleri AssemblyVersionAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkAssembliesWithAssemblyVersion|
|CheckId|CA1016|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Derleme sürüm numarası yok.

## <a name="rule-description"></a>Kural açıklaması

Bir derlemenin kimliğini aşağıdaki bilgilerden oluşur:

- Derleme adı

- Sürüm numarası

- Kültür

- Ortak anahtarı (için kesin adlandırılmış bütünleştirilmiş kodları).

.NET Framework sürüm numarasını derlemeyi benzersiz tanımlamada ve türleri güçlü derlemelere bağlamak için kullanır. Sürüm numarası, sürüm ve yayımcı ilkesi ile birlikte kullanılır. Varsayılan olarak uygulamalar yalnızca oluşturulmuş derleme sürümlerini çalıştırır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için bir sürüm numarası derlemeye kullanarak Ekle <xref:System.Reflection.AssemblyVersionAttribute?displayProperty=fullName> özniteliği. Aşağıdaki örnekte bakın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Üçüncü taraflar tarafından veya bir üretim ortamında kullanılan derlemeler için bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir derlemeye gösterir <xref:System.Reflection.AssemblyVersionAttribute> özniteliği uygulandı.

 [!code-csharp[FxCop.Design.AssembliesVersion#1](../code-quality/codesnippet/CSharp/ca1016-mark-assemblies-with-assemblyversionattribute_1.cs)]
 [!code-vb[FxCop.Design.AssembliesVersion#1](../code-quality/codesnippet/VisualBasic/ca1016-mark-assemblies-with-assemblyversionattribute_1.vb)]
 [!code-cpp[FxCop.Design.AssembliesVersion#1](../code-quality/codesnippet/CPP/ca1016-mark-assemblies-with-assemblyversionattribute_1.cpp)]

## <a name="see-also"></a>Ayrıca bkz.

- [Bütünleştirilmiş Kod Sürümü Oluşturma](/dotnet/framework/app-domains/assembly-versioning)
- [Nasıl yapılır: Yayımcı ilkesi oluşturma](/dotnet/framework/configure-apps/how-to-create-a-publisher-policy)