---
title: 'CA2121: Statik oluşturucular özel | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2121
- StaticConstructorsShouldBePrivate
helpviewer_keywords:
- CA2121
- StaticConstructorsShouldBePrivate
ms.assetid: ee93c620-8fc1-4e47-866c-d389c3ca9f2e
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d7894b4ec0039b28a579239605c22c2397c300f3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68154337"
---
# <a name="ca2121-static-constructors-should-be-private"></a>CA2121: Statik oluşturucular özel olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|StaticConstructorsShouldBePrivate|
|CheckId|CA2121|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Özel olmayan statik Oluşturucu türü vardır.

## <a name="rule-description"></a>Kural Tanımı
 Statik Oluşturucu, bir sınıf oluşturucu olarak da bilinen, bir tür başlatmak için kullanılır. Sistem, türünün ilk örneğinin oluşturulmasından önce statik oluşturucuyu çağırır veya herhangi bir statik üyeye başvurur. Kullanıcının statik Oluşturucu ne zaman çağrıldığını üzerinde denetimi yoktur. Statik oluşturucu özel değilse, sistem dışındaki kod tarafından çağrılabilir. Oluşturucu içinde gerçekleştirilen işlemlere bağlı olarak bu, beklenmeyen davranışlara neden olabilir.

 Bu kural, C# ve Visual Basic .NET derleyiciler tarafından uygulanır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 İhlalleri, genellikle aşağıdaki eylemlerden birini kaynaklanır:

- Statik Oluşturucu türünüz için tanımlanan ve özel göstermedi.

- Programlama dili derleyici türünüz için varsayılan bir statik Oluşturucu eklendi ve özel göstermedi.

  İlk tür ihlalinin düzeltmek için bir statik oluşturucu özel yapın. İkinci tür düzeltmek için türünüz için özel bir statik oluşturucu ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 İhlalleri bastırmayın. Yazılım tasarımı açık bir statik Oluşturucu çağrı gerektiriyorsa, tasarım ciddi sorunlar içeriyor ve gözden geçirilmesi gereken olasıdır.
