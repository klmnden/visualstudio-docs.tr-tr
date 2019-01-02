---
title: 'CA1040: Boş arabirimlerden kaçının'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1040
- AvoidEmptyInterfaces
helpviewer_keywords:
- AvoidEmptyInterfaces
- CA1040
ms.assetid: 120a741b-5fd1-4836-8453-7857e0cd0380
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 8d8691cd2f51cbee2150da05a7421d79d5d602a6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53954162"
---
# <a name="ca1040-avoid-empty-interfaces"></a>CA1040: Boş arabirimlerden kaçının

|||
|-|-|
|TypeName|AvoidEmptyInterfaces|
|CheckId|CA1040|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Arabirim herhangi bir üye bildirmek veya iki veya daha fazla diğer arabirimleri de uygulamak desteklemez.

## <a name="rule-description"></a>Kural açıklaması
 Arayüzler bir davranış veya kullanım sözleşmesi sağlayan üyeleri tanımlar. Arabirim tarafından tanımlanan fonksiyonellik herhangi bir tür tarafından türün kalıtım hiyerarşisinde nerede belirdiği önemsenmeksizin devralınabilir. Tür arabirimin üyeleri için uygulamaları sağlayarak bir arayüz uygular. Boş bir arabirim herhangi bir üye tanımlamıyor. Bu nedenle, uygulanabilir bir sözleşme tanımlamaz.

 Tasarımınızı boş içeriyorsa türleri arabirimleri uygulayan beklenir, büyük olasılıkla bir işaretçi veya bir grup türleri tanımlamak için bir yol olarak bir arabirim kullanıyorsunuz. Bu kimliği, çalışma zamanında meydana gelir, bunu gerçekleştirmek için doğru şekilde özel bir öznitelik kullanmaktır. Hedef türlerini tanımlamak için varlığı veya öznitelik olmaması veya öznitelik özelliklerini kullanın. Ardından derleme zamanında kimliği olmalıdır, boş bir arabirim kullanmak için kabul edilebilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Arabirimi Kaldır veya üyeleri ekleyin. Boş arabirim türleri kümesi etiketlemek için kullanılıyorsa, arabirim özel bir öznitelik ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Arabirimi, derleme zamanında türleri kümesini tanımlamak için kullanıldığında, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, boş bir arabirim gösterir.

 [!code-csharp[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/CSharp/ca1040-avoid-empty-interfaces_1.cs)]
 [!code-cpp[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/CPP/ca1040-avoid-empty-interfaces_1.cpp)]
 [!code-vb[FxCop.Design.InterfacesNotEmpty#1](../code-quality/codesnippet/VisualBasic/ca1040-avoid-empty-interfaces_1.vb)]