---
title: 'CA1725: Parametre adları temel bildirimle eşleşmemelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- ParameterNamesShouldMatchBaseDeclaration
- CA1725
helpviewer_keywords:
- CA1725
- ParameterNamesShouldMatchBaseDeclaration
ms.assetid: 9b657ab0-fe81-4f4c-9481-ba746988c922
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7e6142ff65800e3d31a867ba0fb1ff63afba187b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54973076"
---
# <a name="ca1725-parameter-names-should-match-base-declaration"></a>CA1725: Parametre adları temel bildirimle eşleşmemelidir

|||
|-|-|
|TypeName|ParameterNamesShouldMatchBaseDeclaration|
|CheckId|CA1725|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir yöntem geçersiz bir parametre adı taban yöntemi bildirimini veya yöntemin arabirim bildirimindeki parametrenin adı parametrenin adı eşleşmiyor.

## <a name="rule-description"></a>Kural açıklaması
 Parametreyi geçersiz kılma hiyerarşisinde tutarlı adlandırma yöntemini geçersiz kılmaları kullanılabilirliği artırır. Temel bildirim alanındaki addan farklı türetilmiş yöntem parametre adı taban yöntemini geçersiz kılma veya yeni aşırı yöntemin yöntem olup olmadığı hakkında karışıklığa neden olabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için parametre taban bildirimini eşleşecek şekilde yeniden adlandırın. COM görünür yöntemler için bir değişiklik düzeltmesidir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 COM görünür yöntemleri daha önce sevk kitaplıklarında dışında bu kuraldan bir uyarıyı bastırmayın.