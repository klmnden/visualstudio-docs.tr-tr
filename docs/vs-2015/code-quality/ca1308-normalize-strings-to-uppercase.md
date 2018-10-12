---
title: 'CA1308: dizeleri büyük harfe normalleştirin | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1308
- NormalizeStringsToUppercase
helpviewer_keywords:
- NormalizeStringsToUppercase
- CA1308
ms.assetid: 7e9a7457-3f93-4938-ac6f-1389fba8d9cc
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: eee4a569d7a746a90d8e951b19c86fd0675295ea
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49187511"
---
# <a name="ca1308-normalize-strings-to-uppercase"></a>CA1308: Dizeleri büyük harfe normalleştirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|NormalizeStringsToUppercase|
|CheckId|CA1308|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir işlem, bir dizeyi küçük harfe normalleştirir.

## <a name="rule-description"></a>Kural Tanımı
 Dizeler büyük harfe normalleştirilmeli. Küçük bir grup karakterlerin küçük harfe dönüştürülür, gidiş dönüş yapamaz. Gidiş dönüş yapmak dönüştürülmüş karakterlerinden özgün karakterler karakterleri bir yerel ayardan farklı karakter verileri temsil eden başka bir yerel ayar ve ardından için doğru bir şekilde dönüştürmek için yol alın.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Değiştirme dizelerini küçük harfe dönüştürmek ve böylece dizeleri dönüştürülür işlemleri yerine büyük. Örneğin, değiştirme `String.ToLower(CultureInfo.InvariantCulture)` için `String.ToUpper(CultureInfo.InvariantCulture)`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 (Örneğin, kullanıcı Arabiriminde görüntülemekte olduğunuz) sonucuna dayalı güvenlik kararı yaparken değil, bir uyarı iletisi bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca Bkz.
 [Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)



