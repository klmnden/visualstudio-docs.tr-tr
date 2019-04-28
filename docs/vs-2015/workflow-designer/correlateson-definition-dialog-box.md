---
title: CorrelatesOn tanımı iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- CorrelatesOnDefinition.UI
ms.assetid: 8b2b627a-f236-4479-aa09-525df65e3413
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: fd03e1a8615e75d3f00f79eb10b7a7ff97f0eb33
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977369"
---
# <a name="correlateson-definition-dialog-box"></a>CorrelatesOn Tanımı İletişim Kutusu
**CorrelatesOn** iletişim kutusu kullanılan [!INCLUDE[wfd1](../includes/wfd1-md.md)] düzenlenecek <xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A> özelliği bir <xref:System.ServiceModel.Activities.Receive> etkinlik. [!INCLUDE[crdefault](../includes/crdefault-md.md)] [alma](../workflow-designer/receive-activity-designer.md) konu.  
  
 Arasındaki korelasyon <xref:System.ServiceModel.Activities.Receive> etkinlikleri nasıl farklı hizmet işlemleri bağlanmak birbirleri ile bir iş akışında belirtir.  
  
 Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **CorrelatesOn** iletişim kutusu.  
  
|Arabirim Öğesi|Açıklama|  
|----------------|-----------------|  
|**CorrelatesWith**|<xref:System.ServiceModel.Activities.CorrelationHandle> Uygun iş akışı örneği için ileti yönlendirmek için kullanılır.|  
|**XPath sorguları**|Gelen istenmeyen iletilere bağıntı verileri ayıklamak için kullanılan sorguları içeren bir anahtar/değer çifti. Bu karşılık gelir <xref:System.ServiceModel.Activities.Receive.CorrelatesOn%2A> özelliği. XPath sorguları bulunan bir <xref:System.ServiceModel.MessageQuerySet> nesne.|  
  
## <a name="to-launch-the-correlateson-dialog-box"></a>CorrelatesOn iletişim kutusunu başlatmak için  
 **Alma** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey yerde etkinlikleri genellikle yerleştirilir. Bu, oluşturur bir <xref:System.ServiceModel.Activities.Receive> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> alma. Seçin **alma** etkinlik Tasarımcısı ve üç nokta düğmesini (koleksiyon) metnin yanında tıklatın **CorrelatesOn** özelliği için özellik kılavuzunda **definice vlastnosti Correlateson**  iletişim kutusu görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.ServiceModel.Activities.Receive>   
 [Correlationınitializer Ekle iletişim kutusu](../workflow-designer/add-correlationinitializers-dialog-box.md)   
 [Bağıntıyı Başlat İletişim Kutusu](../workflow-designer/initialize-correlation-dialog-box.md)