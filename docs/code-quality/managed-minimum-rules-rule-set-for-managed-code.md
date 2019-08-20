---
title: Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 44a50c54-8dd3-42b2-8387-532a150e5a6c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 183923a764cc3462e799c8f67677aa564c5fe59d
ms.sourcegitcommit: b83fefa8177c5554cbe2c59c4d102cbc534f7cc6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69585120"
---
# <a name="managed-minimum-rules-rule-set-for-managed-code"></a>Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi

Yönetilen minimum kurallar, olası güvenlik delikleri, uygulama kilitlenmesi ve diğer önemli mantık ve tasarım hataları da dahil olmak üzere kodunuzda en kritik sorunlara odaklanmaktadır. Bu kuralı, projeleriniz için oluşturduğunuz herhangi bir özel kural kümesine ekleyin.

|Kural|Açıklama|
|----------|-----------------|
|[CA1001](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)|Atılabilen alanlara sahip türler atılabilir olmalıdır|
|[CA1821](../code-quality/ca1821-remove-empty-finalizers.md)|Boş sonlandırıcıları kaldırın|
|[CA2213](../code-quality/ca2213-disposable-fields-should-be-disposed.md)|Atılabilen alanlar atılmalıdır|
|[CA2231](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)|Geçersiz kılma için aşırı yükleme işleci eşittir`ValueType.Equals`|
