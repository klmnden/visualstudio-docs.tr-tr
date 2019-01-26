---
title: 'CA2121: Statik oluşturucular özel olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2121
- StaticConstructorsShouldBePrivate
helpviewer_keywords:
- CA2121
- StaticConstructorsShouldBePrivate
ms.assetid: ee93c620-8fc1-4e47-866c-d389c3ca9f2e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 80cc1b3312a4b3c5a53b8b05d8b68064c82d9879
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54960392"
---
# <a name="ca2121-static-constructors-should-be-private"></a>CA2121: Statik oluşturucular özel olmalıdır

|||
|-|-|
|TypeName|StaticConstructorsShouldBePrivate|
|CheckId|CA2121|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Özel olmayan statik Oluşturucu türü vardır.

## <a name="rule-description"></a>Kural açıklaması

Statik Oluşturucu, bir sınıf oluşturucu olarak da bilinen, bir tür başlatmak için kullanılır. Sistem, türünün ilk örneğinin oluşturulmasından önce statik oluşturucuyu çağırır veya herhangi bir statik üyeye başvurur. Kullanıcının statik Oluşturucu ne zaman çağrıldığını üzerinde denetimi yoktur. Statik oluşturucu özel değilse, sistem dışındaki kod tarafından çağrılabilir. Oluşturucu içinde gerçekleştirilen işlemlere bağlı olarak bu, beklenmeyen davranışlara neden olabilir.

Bu kural, C# ve Visual Basic derleyiciler tarafından uygulanır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

İhlalleri, genellikle aşağıdaki eylemlerden birini kaynaklanır:

- Statik Oluşturucu türünüz için tanımlanan ve özel göstermedi.

- Programlama dili derleyici türünüz için varsayılan bir statik Oluşturucu eklendi ve özel göstermedi.

İlk tür ihlalinin düzeltmek için bir statik oluşturucu özel yapın. İkinci tür düzeltmek için türünüz için özel bir statik oluşturucu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

İhlalleri bastırmayın. Yazılım tasarımı açık bir statik Oluşturucu çağrı gerektiriyorsa, tasarım ciddi sorunlar içeriyor ve gözden geçirilmesi gereken olasıdır.