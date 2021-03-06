---
title: 'CA2121: Statik oluşturucular özel olmalıdır'
ms.date: 11/04/2016
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
ms.openlocfilehash: b52f4412b1b048c41033f74200828f70361c1ea3
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232499"
---
# <a name="ca2121-static-constructors-should-be-private"></a>CA2121: Statik oluşturucular özel olmalıdır

|||
|-|-|
|TypeName|StaticConstructorsShouldBePrivate|
|CheckId|CA2121|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Türün özel olmayan bir statik Oluşturucusu vardır.

## <a name="rule-description"></a>Kural açıklaması

Sınıf oluşturucusu olarak da bilinen statik bir Oluşturucu, bir türü başlatmak için kullanılır. Sistem, türünün ilk örneğinin oluşturulmasından önce statik oluşturucuyu çağırır veya herhangi bir statik üyeye başvurur. Statik Oluşturucu çağrıldığında kullanıcının denetimi yoktur. Statik oluşturucu özel değilse, sistem dışındaki kod tarafından çağrılabilir. Oluşturucu içinde gerçekleştirilen işlemlere bağlı olarak bu, beklenmeyen davranışlara neden olabilir.

Bu kural, C# ve Visual Basic derleyicileri tarafından zorlanır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

İhlaller genellikle aşağıdaki eylemlerden biri nedeniyle oluşur:

- Türü için bir statik Oluşturucu tanımladınız ve özel hale gelmedi.

- Programlama dili derleyicisi, türüne varsayılan bir statik Oluşturucu ekledi ve özel hale gelmedi.

İlk ihlalin türünü onarmak için statik oluşturucuyu özel yapın. İkinci türü onarmak için, türünüz için bir özel statik oluşturucu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu ihlalleri engellemez. Yazılım tasarımınız statik bir oluşturucuya açık bir çağrı gerektiriyorsa, tasarımın ciddi kusurlar içermesi ve incelenmesi gerekir.