---
title: Bileşen diyagramlarındaki öğelerin özellikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
f1_keywords:
- vs.teamarch.componentdiagram.shapes.properties
helpviewer_keywords:
- component diagrams, properties
- UML, element properties
ms.assetid: fa0a9460-6675-4642-aa00-50f8719a892d
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c7f3f30d08fb62defec5e783da286e968a6b17c9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63444425"
---
# <a name="properties-of-elements-on-uml-component-diagrams"></a>Bileşen diyagramlarındaki öğelerin özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir UML bileşen diyagramı her öğe diyagram üzerindeki özellikleri vardır. Öğenin özelliklerini görmek için diyagram üzerinde veya öğeye sağ tıklayın **UML Model Gezgini** ve ardından **özellikleri**. Özellikleri görünür **özellikleri** penceresi.  
  
> [!NOTE]
> Bu konu UML Bileşen Diyagramı'ndaki öğelerin özellikleri hakkındadır. UML Bileşen diyagramları okuma hakkında daha fazla bilgi için bkz. [UML Bileşen Diyagramları: Başvuru](../modeling/uml-component-diagrams-reference.md). UML Bileşen diyagramları çizmek hakkında daha fazla bilgi için bkz. [UML Bileşen Diyagramları: Yönergeleri](../modeling/uml-component-diagrams-guidelines.md).  
  
## <a name="properties-of-elements"></a>Öğelerin özellikleri  
  
|Özellik|Varsayılan|Öğe|Açıklama|  
|--------------|-------------|-------------|-----------------|  
|**Ad**|Varsayılan bir ad|Tümü|Öğeyi tanımlar.|  
|**Tam adı**|Namespace:: Ad|Tümü|Öğeyi benzersiz şekilde tanımlar.<br /><br /> Bir bileşen veya türün adını da içeren paket tam adı ile önekidir.<br /><br /> Sahibi bileşenin tam adı ile bir bölümü veya bağlantı noktası adının öneki.|  
|**İş öğeleri**|ilişkili 0|Tümü|Bu öğeyle ilişkili çalışma öğelerinin sayısı. İş öğelerini ilişkilendirmek için bkz: [bağlantı model öğelerini ve iş öğeleri](../modeling/link-model-elements-and-work-items.md).|  
|**Açıklama**|(hiçbiri)|Tümü|Burada bir öğeyle ilgili genel bir not alabilirsiniz.|  
|**Renk**|(varsayılan türü için)|Bileşen, parça, temsilci seçme, parça derlemesi|Şeklin rengi. Diğer özelliklerin aksine, şeklin gösterdiği model öğeyi yerine şeklin rengi budur.|  
|**Dolaylı olarak Örneklendirilmiş**|Doğru|Bileşen|Bileşen yalnızca bir tasarım yapıt yok. Çalışma zamanında, yalnızca bölümleri mevcuttur.|  
|**Özet**|False|Bileşen|Bileşen tanımı, yalnızca diğer bileşenleri özelleştirilebilir Genelleştirme kullanılabilir.|  
|**Görünürlük**|Ortak|Bileşen, parça, bağlantı noktası|**Genel** - Global olarak görünür.<br /><br /> **Paket** - paket içinde görünür.<br /><br /> **Özel** - sahibi olan bileşen içinde görünür.<br /><br /> **Korumalı** - sahibinden türetilen bileşenleri görünür.|  
|**Tür**|Oluşturma türü|Bölümü<br /><br /> Bağlantı Noktası|Bir bölümün bir bileşen ya da sınıf türüdür.<br /><br /> Bir bağlantı noktası bir arabirim türüdür.|  
|**Çokluk**|1.|Bölümü<br /><br /> Bağlantı Noktası|Belirtilen tür bir parçasını oluşturan ana bileşen kaç örneklerini gösterir.<br /><br /> `1` -tam olarak bir.<br /><br /> `0..1` -bir ya da yok.<br /><br /> `*` -herhangi bir sayıdaki bir koleksiyon.<br /><br /> `n..m` -koleksiyonundan n m örnekleri.|  
|**Davranış**|False|Bağlantı Noktası|TRUE ise bu bağlantı için ileti etkinlikleri veya parçalarından yerine bileşen bir parçası olarak açıklanan işlemlerin işlenir.|  
|**Hizmeti**|False|Bağlantı Noktası|TRUE ise, bu bağlantı noktası bu bileşen yayımlanan arabiriminin bir parçasıdır.|  
|**LinkedPackage**|Model|Diyagram|Bu diyagram için eklenen öğeleri varsayılan ad alanı.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UML Kullanım Örneği Diyagramları: Başvuru](../modeling/uml-use-case-diagrams-reference.md)   
 [UML Kullanım Örneği Diyagramları: Yönergeler](../modeling/uml-use-case-diagrams-guidelines.md)
