---
title: Güvenilirlik Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.reliabilityrules
helpviewer_keywords:
- warnings, reliability
- reliability warnings
- managed code analysis warnings, reliability warnings
ms.assetid: 77886846-10a2-4585-968a-7eb60ebe07e8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 009422eaf9ac81af6e8f9d48732655b2528c85a0
ms.sourcegitcommit: 92a04c57ac0a49f304fa2ea5043436f30068c3cd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2019
ms.locfileid: "65976145"
---
# <a name="reliability-warnings"></a>Güvenilirlik uyarıları

Güvenilirlik uyarıları doğru bellek ve iş parçacığı kullanımı gibi kitaplık ve uygulama güvenilirliği destekler. Güvenilirlik kuralları şunlardır:

|Kural|Açıklama|
|----------|-----------------|
|[CA2000: Kapsamı kaybetmeden önce verileri nesneleri dispose](../code-quality/ca2000-dispose-objects-before-losing-scope.md)|Bir nesnenin sonlandırıcısının çalışmasını engelleyecek olağanüstü bir durum gerçekleşebileceği için, nesne ona olan tüm başvurular kapsam dışına çıkmadan açıkça atılmalıdır.|
|[CA2001: Sorunlu yöntemleri çağırmaktan kaçının](../code-quality/ca2001-avoid-calling-problematic-methods.md)|Bir üye olası tehlikeli ya da sorunlu yöntemi çağırır.|
|[CA2002: Zayıf kimliği olan nesneleri kilitlemeyin](../code-quality/ca2002-do-not-lock-on-objects-with-weak-identity.md)|Bir nesneye uygulama etki alanları arasından erişilebiliyorsa o nesnenin zayıf bir kimliğe sahip olduğu söylenir. Zayıf kimliğe sahip bir nesne üzerinde kilit almayı deneyen iş parçacığı aynı nesne üzerinde bir kilide sahip olan farklı uygulama etki alanı içindeki ikinci iş parçacığı tarafından engellenebilir.|
|[CA2003: Lifleri iş parçacığı olarak değil](../code-quality/ca2003-do-not-treat-fibers-as-threads.md)|Yönetilen iş parçacığı bir Win32 iş parçacığı kabul edilir.|
|[CA2004: GC kaldırın. KeepAlive](../code-quality/ca2004-remove-calls-to-gc-keepalive.md)|SafeHandle kullanımını dönüştürüyorsanız, GC tüm çağrıları kaldırın. KeepAlive (nesne). Bu durumda, GC çağırmak sınıflar olmamalıdır. Bir sonlandırıcı olmayan ancak işletim sistemi sonlandırmak için SafeHandle üzerinde dayanır varsayılarak KeepAlive, bunlar için işler.|
|[CA2006: Yerel kaynakları kapsamak için SafeHandle kullanın](../code-quality/ca2006-use-safehandle-to-encapsulate-native-resources.md)|Yönetilen kod içinde IntPtr kullanmak olası bir güvenlik ve güvenilirlik sorunu belirtebilir. IntPtr'nin tüm kullanımları onun yerine bir SafeHandle ya da benzer bir teknolojinin kullanımının gerekip gerekmediğini belirlemek için gözden geçirilmelidir.|
|[CA2007: Doğrudan göreve await değil](../code-quality/ca2007-do-not-directly-await-task.md)|Zaman uyumsuz bir yöntem [bekler](/dotnet/csharp/language-reference/keywords/await) bir <xref:System.Threading.Tasks.Task> doğrudan.|