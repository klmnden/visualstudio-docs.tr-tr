---
title: UML öğeleri özelliklerini örneği diyagramları kullanma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
f1_keywords:
- vs.teamarch.usecasediagram.artifact.properties
- vs.teamarch.usecasediagram.shapes.properties
helpviewer_keywords:
- use case diagrams, properties
ms.assetid: 2728fb26-a275-4fce-8a2c-5a78af6bee04
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: dbe2a9f3d46be72ae1e463da7c6173ef0571bc89
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54762003"
---
# <a name="properties-of-elements-on-uml-use-case-diagrams"></a>UML kullanım durumu diyagramlarındaki öğelerin özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

UML Kullanım durumu diyagramında, her öğe diyagram üzerindeki özellikleri vardır. Öğenin özelliklerini görmek için diyagram üzerinde veya öğeye sağ tıklayın **UML Model Gezgini** ve ardından **özellikleri**. Özellikleri görünür **özellikleri** penceresi.  
  
> [!NOTE]
>  Bu konu UML Kullanım durumu diyagramlarındaki öğelerin özellikleri hakkındadır. UML etkinlik diyagramları okuma hakkında daha fazla bilgi için bkz. [UML Kullanım durumu diyagramları: Başvuru](../modeling/uml-use-case-diagrams-reference.md). UML etkinlik diyagramları çizmek hakkında daha fazla bilgi için bkz. [UML Kullanım durumu diyagramları: Yönergeleri](../modeling/uml-use-case-diagrams-guidelines.md).  
  
## <a name="properties-of-elements"></a>Öğelerin özellikleri  
  
|Özellik|Varsayılan|Öğe|Açıklama|  
|--------------|-------------|-------------|-----------------|  
|**Ad**|Varsayılan bir ad|Tümü|Öğeyi tanımlar.|  
|**Tam adı**|Paket:: Ad|Tümü|Öğeyi benzersiz şekilde tanımlar. İle içerdiği paket tam adı öneki.|  
|**İş öğeleri**|ilişkili 0|Tümü|Bu öğeyle ilişkili çalışma öğelerinin sayısı. İş öğelerini ilişkilendirmek için bkz: [bağlantı model öğelerini ve iş öğeleri](../modeling/link-model-elements-and-work-items.md).|  
|**Açıklama**|(hiçbiri)|Tümü|Burada bir öğeyle ilgili genel bir not alabilirsiniz.|  
|**Renk**|(varsayılan)|Tümü|Şeklin rengi. Diğer özelliklerin aksine, bu olmadığından, bir özellik öğesinin şeklini görüntüler.|  
|**Görüntü yolu**|(hiçbiri)|Aktör|Görüntünün varsayılan aktör simge yerine kullanılması gereken dosya yolu. Simgesi, Visual Studio projesi içinde bir kaynak dosyası olmalıdır.|  
|**Konuları**|(hiçbiri)|Kullanım Örneği|Veya alt kullanım örneği başka bir türü.<br /><br /> Kullanım örneği diyagramındaki bir alt sisteminde yerleştirerek ayarlayabilirsiniz.|  
|**Görünürlük**|Ortak|Örneği, aktör, alt kullanın|**Genel** - Global olarak görünür.<br /><br /> **Paket** - paket içinde görünür.|  
|**IsAbstract**|False|Örneği, aktör, alt kullanın|TRUE ise, türü oluşturulamaz ve diğer tanımları tarafından özelleştirmesi için temel olarak tasarlanmıştır.|  
|**Dolaylı olarak Örneklendirilmiş**|Doğru|Alt sistem|Alt yalnızca bir tasarım yapıt bulunmaktadır. Çalışma zamanında, yalnızca bölümleri mevcuttur.|  
|**Köprü**|(hiçbiri)|Yapıt|Diyagram veya belge yapıt bağlantı sağlayan URL veya dosya yolu.|  
  
 İlişkilendirmelerin özelliklerinin bir listesi için bkz. [UML İlişkilendirmelerin Özellikleri sınıf diyagramları](../modeling/properties-of-associations-on-uml-class-diagrams.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UML Kullanım durumu diyagramları: Başvuru](../modeling/uml-use-case-diagrams-reference.md)   
 [UML Kullanım durumu diyagramları: Yönergeleri](../modeling/uml-use-case-diagrams-guidelines.md)
