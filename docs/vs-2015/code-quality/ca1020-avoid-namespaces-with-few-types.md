---
title: 'CA1020: Birkaç türü olan ad alanlarından kaçının | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1020
- AvoidNamespacesWithFewTypes
helpviewer_keywords:
- CA1020
- AvoidNamespacesWithFewTypes
ms.assetid: 9cb272f6-a3ff-45af-b35d-70dea620b074
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 8c94cf09b43eb09482be4a30d9f0b9206678c4dc
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63435839"
---
# <a name="ca1020-avoid-namespaces-with-few-types"></a>CA1020: Az tür içeren ad alanlarından kaçının
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|AvoidNamespacesWithFewTypes|
|CheckId|CA1020|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Genel ad başka bir ad alanı Beşten az türleri içerir.

## <a name="rule-description"></a>Kural Tanımı
 Her ad alanlarınıza mantıksal düzenlemesi vardır ve seyrek doldurulmuş bir ad alanına türleri koymak için geçerli bir nedeni var olduğundan emin olun. Ad alanları, birlikte Çoğu senaryoda kullanılan türler içermelidir. Uygulamalarını karşılıklı olarak birbirini dışlar, ayrı ad alanlarında türleri bulunmalıdır. Örneğin, <xref:System.Web.UI> ad alanı, Web uygulamalarında kullanılan türler içerir ve <xref:System.Windows.Forms> ad alanı olarak kullanılan türler içerir [!INCLUDE[TLA#tla_mswin](../includes/tlasharptla-mswin-md.md)]-tabanlı uygulamaları. Kullanıcı arabirimi özelliklerini denetleyen türleri her iki ad alanına sahip olsa da, bu türleri aynı uygulamada kullanılmak üzere tasarlanmamıştır. Bu nedenle, bunlar ayrı ad alanlarında bulunur. Bir özelliğin bulunabilirliğini artıracağı için dikkatli ad kuruluş de yararlı olabilir. Ad alanı hiyerarşisi inceleyerek kitaplığı tüketicileri bir özelliği uygulayan türler bulabilir olması gerekir.

> [!NOTE]
> Tasarım zamanı türlerinde ve izinlerde bu kılavuzu ile uyum sağlamak için diğer ad alanları içine birleştirilmesini değil. Bu tür, kendi ad alanlarında, ana ad alanının altındaki ait ve ad alanlarını bitmelidir `.Design` ve `.Permissions`sırasıyla.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için tek bir ad alanına birkaç türlerini içeren ad alanları birleştirmek deneyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Ad alanı, diğer ad alanlarında türleri ile kullanılan türler içermediğinde bu kuraldan bir uyarıyı bastırmak güvenlidir.
