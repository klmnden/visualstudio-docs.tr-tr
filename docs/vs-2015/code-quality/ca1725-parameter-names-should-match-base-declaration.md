---
title: 'CA1725: Parametre adları taban eşleşmelidir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- ParameterNamesShouldMatchBaseDeclaration
- CA1725
helpviewer_keywords:
- CA1725
- ParameterNamesShouldMatchBaseDeclaration
ms.assetid: 9b657ab0-fe81-4f4c-9481-ba746988c922
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e97431b46640fb8241d6bde80d09d38084650be8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794898"
---
# <a name="ca1725-parameter-names-should-match-base-declaration"></a>CA1725: Parametre adları temel bildirimle eşleşmemelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ParameterNamesShouldMatchBaseDeclaration|
|CheckId|CA1725|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir yöntem geçersiz bir parametre adı taban yöntemi bildirimini veya yöntemin arabirim bildirimindeki parametrenin adı parametrenin adı eşleşmiyor.

## <a name="rule-description"></a>Kural Tanımı
 Parametreyi geçersiz kılma hiyerarşisinde tutarlı adlandırma yöntemini geçersiz kılmaları kullanılabilirliği artırır. Temel bildirim alanındaki addan farklı türetilmiş yöntem parametre adı taban yöntemini geçersiz kılma veya yeni aşırı yöntemin yöntem olup olmadığı hakkında karışıklığa neden olabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için parametre taban bildirimini eşleşecek şekilde yeniden adlandırın. COM görünür yöntemler için bir değişiklik düzeltmesidir.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 COM görünür yöntemleri daha önce sevk kitaplıklarında dışında bu kuraldan bir uyarıyı bastırmayın.
