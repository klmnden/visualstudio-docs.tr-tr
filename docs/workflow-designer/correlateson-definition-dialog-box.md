---
title: İş Akışı Tasarımcısı - CorrelatesOn tanımı iletişim kutusu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CorrelatesOnDefinition.UI
ms.assetid: 8b2b627a-f236-4479-aa09-525df65e3413
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cba12e3e991282dc69ea5747d62db8761d6f8d16
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55942641"
---
# <a name="correlateson-definition-dialog-box"></a>CorrelatesOn Tanımı İletişim Kutusu

**CorrelatesOn** iletişim kutusunda iş akışı Tasarımcısı'nda düzenlemek için kullanılan <xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A> özelliği bir <xref:System.ServiceModel.Activities.Receive> etkinlik. Daha fazla bilgi için [alma etkinlik Tasarımcısı](../workflow-designer/receive-activity-designer.md).

Arasındaki korelasyon <xref:System.ServiceModel.Activities.Receive> etkinlikleri nasıl farklı hizmet işlemleri bağlanmak birbirleri ile bir iş akışında belirtir.

Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **CorrelatesOn** iletişim kutusu.

|Arabirim Öğesi|Açıklama|
|-|-----------------|
|**CorrelatesWith**|<xref:System.ServiceModel.Activities.CorrelationHandle> Uygun iş akışı örneği için ileti yönlendirmek için kullanılır.|
|**XPath sorguları**|Gelen istenmeyen iletilere bağıntı verileri ayıklamak için kullanılan sorguları içeren bir anahtar/değer çifti. Bu değer karşılık gelen <xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A> özelliği. XPath sorguları bulunan bir <xref:System.ServiceModel.MessageQuerySet> nesne.|

## <a name="to-launch-the-correlateson-dialog-box"></a>CorrelatesOn iletişim kutusunu başlatmak için

**Alma** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve etkinlikleri genellikle yerleştirilen her yerde iş akışı Tasarımcısı yüzeyine açın. Etkinlik Tasarımcısı bırakarak oluşturur bir <xref:System.ServiceModel.Activities.Receive> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> alma. Açmak için **definice vlastnosti Correlateson** iletişim kutusunda **alma** etkinlik Tasarımcısı ve sonra özellik kılavuzunda seçmek için koleksiyon ifadesinin yanındaki üç nokta düğmesini  **CorrelatesOn** özelliği.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.Activities.Receive>
- [CorrelationInitializer Ekle İletişim Kutusu](../workflow-designer/add-correlationinitializers-dialog-box.md)
- [Bağıntı iletişim kutusu Ekle](http://msdn.microsoft.com/en-us/9e41a149-e8ab-41b1-8886-ea06a63041b6)
- [Bağıntıyı Başlat İletişim Kutusu](../workflow-designer/initialize-correlation-dialog-box.md)