---
title: "CA2115: Yerel kaynaklar kullanırken GC.KeepAlive'ı çağırın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CallGCKeepAliveWhenUsingNativeResources
- CA2115
helpviewer_keywords:
- CA2115
- CallGCKeepAliveWhenUsingNativeResources
ms.assetid: f00a59a7-2c6a-4bbe-a1b3-7bf77d366f34
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: eb6d28e15870907034479e698ba8e7464f4f5159
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232719"
---
# <a name="ca2115-call-gckeepalive-when-using-native-resources"></a>CA2115: Yerel kaynaklar kullanırken GC.KeepAlive'ı çağırın

|||
|-|-|
|TypeName|CallGCKeepAliveWhenUsingNativeResources|
|CheckId|CA2115|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Sonlandırıcıyı içeren bir tür içinde belirtilen bir yöntem, <xref:System.IntPtr?displayProperty=fullName> veya <xref:System.UIntPtr?displayProperty=fullName> alanına başvurur, ancak çağırmaz <xref:System.GC.KeepAlive%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

Yönetilen kodda kendisine daha fazla başvuru yoksa çöp toplama bir nesneyi sonlandırır. Nesnelere yönetilmeyen başvurular çöp toplamayı engellemez. Bu kural, yönetimsiz kod içinde kullanıldığı sırada yönetilmeyen kaynağın sonlandırılması nedeniyle oluşabilecek hataları algılar.

Bu kural, <xref:System.IntPtr> ve <xref:System.UIntPtr> alanlarının, yönetilmeyen kaynaklara işaretçiler depodığını varsayar. Sonlandırıcının amacı, yönetilmeyen kaynakları serbest yönlendirtiğinden, bu, sonlandırıcının işaretçi alanları tarafından işaret edilen yönetilmeyen kaynağı serbest olarak kabul ettiği varsayılır. Bu kural ayrıca yöntemin yönetilmeyen kaynağa yönetilmeyen koda iletilmesi için işaretçi alanına başvuracağını varsayar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için yöntemine bir çağrı <xref:System.GC.KeepAlive%2A> ekleyin, geçerli örneği bağımsız değişken olarak geçirerek (`this` ve C# C++içinde). Çağrıyı, nesnenin çöp toplamadan korunması gereken son kod satırından sonra konumlandırın. <xref:System.GC.KeepAlive%2A>' A yapılan çağrıdan hemen sonra nesne, kendisine yönetilen başvuru olmadığı varsayılarak çöp toplama için hazır olarak kabul edilir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kural, yanlış pozitiflere yol açabilecek bazı varsayımlar yapar. Şu durumlarda bu kuraldan bir uyarıyı güvenle gizleyebilirsiniz:

- Sonlandırıcı, yöntemi tarafından başvurulan <xref:System.IntPtr> veya <xref:System.UIntPtr> alanının içeriğini serbest vermez.

- Yöntemi, <xref:System.IntPtr> veya <xref:System.UIntPtr> alanını yönetilmeyen koda iletmez.

Diğer iletileri hariç tutarak dikkatle gözden geçirin. Bu kural, yeniden oluşturulması ve hata ayıklaması zor olan hataları algılar.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, `BadMethod` öğesine `GC.KeepAlive` bir çağrı içermez ve bu nedenle kuralı ihlal eder. `GoodMethod`düzeltilen kodu içerir.

> [!NOTE]
> Bu örnek sözde koddur. Kodu oluşturulup çalıştırmakla birlikte, yönetilmeyen bir kaynak oluşturulmadığından veya serbest bırakıldığı için uyarı tetiklenmez.

[!code-csharp[FxCop.Security.IntptrAndFinalize#1](../code-quality/codesnippet/CSharp/ca2115-call-gc-keepalive-when-using-native-resources_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.GC.KeepAlive%2A?displayProperty=fullName>
- <xref:System.IntPtr?displayProperty=fullName>
- <xref:System.Object.Finalize%2A?displayProperty=fullName>
- <xref:System.UIntPtr?displayProperty=fullName>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)