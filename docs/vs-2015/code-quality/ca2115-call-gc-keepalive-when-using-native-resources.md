---
title: 'CA2115: GC çağırın. Yerel kaynaklar kullanırken KeepAlive | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CallGCKeepAliveWhenUsingNativeResources
- CA2115
helpviewer_keywords:
- CA2115
- CallGCKeepAliveWhenUsingNativeResources
ms.assetid: f00a59a7-2c6a-4bbe-a1b3-7bf77d366f34
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0eadff91e8762349ec95c2d9f3bf5717bfecaa4a
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63435030"
---
# <a name="ca2115-call-gckeepalive-when-using-native-resources"></a>CA2115: Yerel kaynaklar kullanırken GC.KeepAlive'ı çağırın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|CallGCKeepAliveWhenUsingNativeResources|
|CheckId|CA2115|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir yöntem bir sonlandırıcı bir türle bildirilen başvuran bir <xref:System.IntPtr?displayProperty=fullName> veya <xref:System.UIntPtr?displayProperty=fullName> alan, ancak arama <xref:System.GC.KeepAlive%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 Yönetilen kodda daha fazla hiçbir başvurusu, atık toplama bir nesne sonlandırır. Yönetilmeyen nesnelere başvurular atık toplama engellemez. Bu kural, yönetimsiz kod içinde kullanıldığı sırada yönetilmeyen kaynağın sonlandırılması nedeniyle oluşabilecek hataları algılar.

 Bu kural, varsayar <xref:System.IntPtr> ve <xref:System.UIntPtr> alanları yönetilmeyen kaynakları işaretçileri depolayın. Bir sonlandırıcı amacı yönetilmeyen kaynakları serbest bırakacak olduğundan kural Sonlandırıcı işaretçi alanlara göre işaret yönetilmeyen kaynağı boşaltır varsayar. Bu kural, ayrıca yöntemi yönetilmeyen koda yönetilmeyen kaynağı geçirmek işaretçi alan başvurulduğu varsayar.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için bir çağrı ekleyin <xref:System.GC.KeepAlive%2A> geçerli örnek yöntemine geçirerek (`this` C# ve C++'ta) bağımsız değişken olarak. Çağrı nesnenin çöp koleksiyonundan burada korunması gereken son kod satırının sonra konumlandırın. Çağırdıktan hemen sonra <xref:System.GC.KeepAlive%2A>, yönetilen hiçbir başvurusu yok varsayarak nesne yeniden çöp toplama işlemi için hazır olarak kabul edilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kural, hatalı pozitif sonuçları için yol açabilecek bazı varsayımlarda bulunur. Ayrıca, güvenli bir şekilde bu kuraldan bir uyarıyı gizleyebilirsiniz:

- Sonlandırıcı içeriğini boş olmayan <xref:System.IntPtr> veya <xref:System.UIntPtr> yöntemi tarafından başvurulan alan.

- Yöntem geçemezse <xref:System.IntPtr> veya <xref:System.UIntPtr> yönetilmeyen kod alanı.

  Diğer iletiler hariç önce dikkatle inceleyin. Bu kural, yeniden oluşturmak ve hatalarını ayıklamak zor olan hataları algılar.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, `BadMethod` çağrısı içermez `GC.KeepAlive` ve bu nedenle kuralı ihlal ediyor. `GoodMethod` Düzeltilen kod içerir.

> [!NOTE]
> Kod derlenir ve çalışır ancak bu örnekte sahte kod, yönetilmeyen bir kaynağı oluşturan veya serbest yüklenmediğinden uyarı tetiklendiğinde değil.

 [!code-csharp[FxCop.Security.IntptrAndFinalize#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.IntptrAndFinalize/cs/FxCop.Security.IntptrAndFinalize.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.GC.KeepAlive%2A?displayProperty=fullName><xref:System.IntPtr?displayProperty=fullName>
 <xref:System.Object.Finalize%2A?displayProperty=fullName>
 <xref:System.UIntPtr?displayProperty=fullName>
 [Dispose Deseni](http://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
