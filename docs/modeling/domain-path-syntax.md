---
title: Etki Alanı Yolu Sözdizimi
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, domain path
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 47c2adc2894cc67b337243c30f4a62bc3642ff39
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55955238"
---
# <a name="domain-path-syntax"></a>Etki Alanı Yolu Sözdizimi
DSL tanımlarına XPath benzeri bir sözdizimi bir modelde belirli öğeleri bulmak için kullanın.

 Normalde bu sözdizimi ile doğrudan çalışmak zorunda değildir. DSL ayrıntıları veya Özellikler penceresinde göründüğü aşağı oka tıklayın ve yolu Düzenleyicisi'ni kullanın. Ancak, düzenleyici kullandıktan sonra yol bu alanı formda görüntülenir.

 Bir etki alanı yolu aşağıdaki biçimi alır:

 *RelationshipName.PropertyName/! Rol*

 ![CommentReferencesSubjects başvuru ilişkisi](../modeling/media/dsl_reference.png)

 Sözdizimi ağacı modelinin erişir. Örneğin, etki alanı ilişkisi **CommentReferencesSubjects** Yukarıdaki örnekteki sahip bir **konuları** rol. Yol kesimi **/! Subjectt** yolu üzerinden erişilen öğeleri tamamlandığını belirtir **konuları** rol.

 Her segmentinde bir etki alanı ilişkisi adı ile başlar. Geçişi öğeden bir ilişki, yol kesimi olarak görünür *Relationship.PropertyName*. Atlama bağlantı için bir öğe, yol kesimi olarak görünür *ilişki /! RoleName*.

 Eğik bir yolu sözdizimi ayırın. Her yol kesimi ya da bir atlama bir öğeye bir bağlantı (bir ilişkinin örneğini) veya bir öğe için bir bağlantı var. Yol kesimleri sık çiftler halinde görünür. Bir yol kesimini bir atlama öğeden bağlantısını temsil eder ve sonraki kesimini bir atlama bağlantıdan diğer uçtaki öğeyi temsil eder. (Tüm bağlantı de kaynak veya hedef bir ilişkinin olabilir).

 Öğe bağlantısı atlama için kullandığınız adı rolün değeri `Property Name`. Link öğesi atlama için kullandığınız ad hedef rol adı değil.

## <a name="see-also"></a>Ayrıca Bkz.

- [Modelleri, Sınıfları ve İlişkileri Anlama](../modeling/understanding-models-classes-and-relationships.md)