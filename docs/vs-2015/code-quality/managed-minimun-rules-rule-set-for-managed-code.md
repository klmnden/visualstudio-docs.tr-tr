---
title: Yönetilen kod için yönetilen minimum kurallar kural kümesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
ms.assetid: 44a50c54-8dd3-42b2-8387-532a150e5a6c
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: fbbbdf8a1ece9a57d0216a6c9b59ac9d2a8ea474
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54761055"
---
# <a name="managed-minimun-rules-rule-set-for-managed-code"></a>Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yönetilen Minimum kurallar potansiyel güvenlik boşluklarını, uygulama kilitlenmesi ve diğer önemli mantık ve tasarım hataları gibi kodunuzda en kritik sorunlara odaklanır. Projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.  
  
|Kural|Açıklama|  
|----------|-----------------|  
|[CA1001](../code-quality/ca1001-types-that-own-disposable-fields-should-be-disposable.md)|Atılabilen alanlara sahip türler atılabilir olmalıdır|  
|[CA1821](../code-quality/ca1821-remove-empty-finalizers.md)|Boş sonlandırıcıları kaldırın|  
|[CA2213](../code-quality/ca2213-disposable-fields-should-be-disposed.md)|Atılabilen alanlar atılmalıdır|  
|[CA2231](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)|Eşittir işlecini ValueType.Equals'ı geçersiz kılarak aşırı yükleyin|
