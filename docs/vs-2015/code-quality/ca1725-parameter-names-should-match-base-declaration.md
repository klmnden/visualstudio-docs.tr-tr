---
title: 'CA1725: Parametre adları temel bildirimle eşleşmemelidir | Microsoft Docs'
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
ms.openlocfilehash: a7ee2253d01f219bb427d3b23d67112c13c71a86
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49206901"
---
# <a name="ca1725-parameter-names-should-match-base-declaration"></a>CA1725: Parametre adları taban yöntem ile eşleşmelidir
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



