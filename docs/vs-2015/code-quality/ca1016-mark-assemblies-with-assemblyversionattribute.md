---
title: 'CA1016: Derlemeleri AssemblyVersionAttribute ile işaretleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- MarkAssembliesWithAssemblyVersion
- CA1016
helpviewer_keywords:
- CA1016
- MarkAssembliesWithAssemblyVersion
ms.assetid: 4340aed8-d92b-4cde-a398-cb6963c6da5a
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4fbe2ef81dbb1dd5be15b6a0ac4b8cc1df96206a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62424017"
---
# <a name="ca1016-mark-assemblies-with-assemblyversionattribute"></a>CA1016: Derlemeleri AssemblyVersionAttribute ile işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkAssembliesWithAssemblyVersion|
|CheckId|CA1016|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Derleme sürüm numarası yok.

## <a name="rule-description"></a>Kural Tanımı
 Bir derlemenin kimliğini aşağıdaki bilgilerden oluşur:

- Derleme adı

- Sürüm numarası

- Kültür

- Ortak anahtarı (için kesin adlandırılmış bütünleştirilmiş kodları).

  [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] Derlemeyi benzersiz tanımlamada ve türleri güçlü derlemelere bağlamak için sürüm numarasını kullanır. Sürüm numarası, sürüm ve yayımcı ilkesi ile birlikte kullanılır. Varsayılan olarak uygulamalar yalnızca oluşturulmuş derleme sürümlerini çalıştırır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için bir sürüm numarası derlemeye kullanarak Ekle <xref:System.Reflection.AssemblyVersionAttribute?displayProperty=fullName> özniteliği. Aşağıdaki örnekte bakın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Üçüncü taraflar tarafından veya bir üretim ortamında kullanılan derlemeler için bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir derlemeye gösterir <xref:System.Reflection.AssemblyVersionAttribute> özniteliği uygulandı.

 [!code-cpp[FxCop.Design.AssembliesVersion#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/cpp/FxCop.Design.AssembliesVersion.cpp#1)]
 [!code-csharp[FxCop.Design.AssembliesVersion#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/cs/FxCop.Design.AssembliesVersion.cs#1)]
 [!code-vb[FxCop.Design.AssembliesVersion#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesVersion/vb/FxCop.Design.AssembliesVersion.vb#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Derleme sürümlendirme](http://msdn.microsoft.com/library/775ad4fb-914f-453c-98ef-ce1089b6f903) [nasıl yapılır: Yayımcı ilkesi oluşturma](http://msdn.microsoft.com/library/8046bc5d-2fa9-4277-8a5e-6dcc96c281d9)
