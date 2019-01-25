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
ms.openlocfilehash: c4f788a69d2be5aa7125c4ca19cb2cab4bf05a04
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54800842"
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
 [Bağıntı iletişim kutusu Ekle](http://msdn.microsoft.com/9e41a149-e8ab-41b1-8886-ea06a63041b6)   
 [Bağıntıyı Başlat İletişim Kutusu](../workflow-designer/initialize-correlation-dialog-box.md)