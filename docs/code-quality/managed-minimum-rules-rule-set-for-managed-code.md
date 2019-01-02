---
title: Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
ms.assetid: 44a50c54-8dd3-42b2-8387-532a150e5a6c
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 56d8528a5a419eb23b1192ef265f70ea536cfe48
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53890449"
---
# <a name="managed-minimum-rules-rule-set-for-managed-code"></a>Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi

Yönetilen Minimum kurallar potansiyel güvenlik boşluklarını, uygulama kilitlenmesi ve diğer önemli mantık ve tasarım hataları gibi kodunuzda en kritik sorunlara odaklanır. Projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesi içerir.

|Kural|Açıklama|
|----------|-----------------|
|[CA1001](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)|Atılabilir alanlara sahip türler atılabilir olmalıdır|
|[CA1821](../code-quality/ca1821-remove-empty-finalizers.md)|Boş Sonlandırıcıları kaldırın|
|[CA2213](../code-quality/ca2213-disposable-fields-should-be-disposed.md)|Atılabilen alanlar atılmalıdır|
|[CA2231](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)|Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde|
