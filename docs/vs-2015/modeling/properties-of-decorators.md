---
title: Dekoratörlerin özellikleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: reference
helpviewer_keywords:
- Domain-Specific Language, decorators
ms.assetid: f6322fe5-dc08-4d32-a6b3-0bd18879136d
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d9cd07ed41e39c931e67f43f1c77ff8bd56b2eb3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701772"
---
# <a name="properties-of-decorators"></a>Dekoratörlerin Özellikleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dekoratörler simgeler, metin veya şekil veya diyagram üzerinde bağlayıcı görünebilir Genişlet/Daralt ayraç ' dir. Aşağıdaki tablolar, dekoratör üç tür özelliklerini gösterir. Bazı özellikler, yalnızca şekli dekoratörler veya yalnızca bağlayıcı dekoratörler görünür.  
  
 Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md). Bu özellikler kullanma hakkında daha fazla bilgi için bkz. [bir etki alanına özgü dili özelleştirme ve genişletme](../modeling/customizing-and-extending-a-domain-specific-language.md).  
  
## <a name="expandcollapse-decorator"></a>Dekoratör Genişlet/Daralt  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|displayName|Oluşturulan tasarımcıda görüntülenecek dekoratörün adı.|Daralt Dekoratör genişletin|  
|Ad|Dekoratörün adı.|ExpandCollapseDecorator|  
|Notlar|Bu dekoratör ile ilişkili resmi olmayan notlar.|\<yok >|  
|HorizontalOffset|Dekoratörün varsayılan konumuna inç cinsinden yatay uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|VerticalOffset|İnç, dekoratörün varsayılan konumuna göre dikey uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|OffsetFromLine|Dekoratörün satırından inç, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|OffsetFromShape|Dekoratörün şekilden inç cinsinden, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|Konum|Dekoratörün varsayılan konumuna.|SourceTop|  
  
## <a name="icon-decorator"></a>Dekoratör simgesi  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|DefaultIcon|Görüntülenecek simge veya resim dosyasının yolu.|\<yok >|  
|displayName|Oluşturulan tasarımcıda görüntülenecek dekoratörün adı.|Dekoratör simgesi|  
|Ad|Dekoratörün adı.|Şeklindeki Icondecorator|  
|Notlar|Dekoratör ile ilişkili resmi olmayan notlar.|\<yok >|  
|HorizontalOffset|Dekoratörün varsayılan konumuna inç cinsinden yatay uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|VerticalOffset|İnç, dekoratörün varsayılan konumuna göre dikey uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|OffsetFromLine|Dekoratörün satırından inç, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|OffsetFromShape|Dekoratörün şekilden inç cinsinden, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|Konum|Dekoratörün varsayılan konumuna.|SourceTop|  
  
## <a name="textdecorator"></a>TextDecorator  
  
|Özellik|Açıklama|Varsayılan|  
|--------------|-----------------|-------------|  
|DefaultText|Görüntülenecek varsayılan metin.|Etiketle|  
|displayName|Oluşturulan tasarımcıda görüntülenecek dekoratörün adı.|Etiketle|  
|FontSize|Dekoratörde görüntülenen metnin yazı tipi boyutu.|8|  
|fontStyle|Dekoratörde görüntülenen metnin yazı tipi stili.|Normal|  
|Ad|Dekoratörün adı.|Etiketle|  
|Notlar|Dekoratör ile ilişkili resmi olmayan notlar.|\<yok >|  
|HorizontalOffset|Dekoratörün varsayılan konumuna inç cinsinden yatay uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|VerticalOffset|İnç, dekoratörün varsayılan konumuna göre dikey uzaklık. (Şekiller üzerinde yalnızca.)|0|  
|OffsetFromLine|Dekoratörün satırından inç, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|OffsetFromShape|Dekoratörün şekilden inç cinsinden, varsayılan konumuna göre uzaklığı. (Bağlayıcı üzerinde yalnızca.)|0|  
|Konum|Dekoratörün varsayılan konumuna.|TargetBottom|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etki alanına özgü dil araçları sözlüğü](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)
