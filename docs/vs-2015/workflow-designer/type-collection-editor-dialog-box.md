---
title: Tür Koleksiyonu Düzenleyicisi iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- TypeCollectionEditor.UI
ms.assetid: 63cdea6b-bca2-4c06-b8b4-c8faabd40726
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: be2e6bde6c25c1bb515ec3f017f14506c03a3a71
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697063"
---
# <a name="type-collection-editor-dialog-box"></a>Tür Koleksiyonu Düzenleyicisi İletişim Kutusu
**Editor Typu Kolekce** iletişim kutusu için bilinen türleri eklemek için kullanılan **Gönder** ve **alma** etkinlikler. Bu iletişim için genel tür bağımsız değişkeni eklemek için de kullanılır **InvokeMethod** etkinlik. İçin kullanıldığında **Gönder** ve **alma** bilinen türleri eklenecek etkinlikleri **Editor Typu Kolekce** iletişim kutusu türü eklemeleri benzersiz olmasını gerektirir. Yinelenen tür eklenir ve değişiklik tıklayarak kararlıdır **Tamam**, bir hata iletisi döndürülür. İçin kullanıldığında **InvokeMethod** genel tür bağımsız değişkenleri, eklemek için etkinlik **Editor Typu Kolekce** yinelenen türlerinin eklenmesi iletişim kutusu sağlar.  
  
> [!NOTE]
> [!INCLUDE[crabout](../includes/crabout-md.md)] bilinen türler, bkz: [veri sözleşme bilinen türleri](https://msdn.microsoft.com/library/1a0baea1-27b7-470d-9136-5bbad86c4337).  
  
 Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **türü koleksiyonu** iletişim kutusu.  
  
|Arabirim Öğesi|Açıklama|  
|----------------|-----------------|  
|**Tür Listesi**|Eklenen veya kaldırılan türlerinin listesi.|  
  
## <a name="to-bring-up-the-type-collection-editor"></a>Editor Typu Kolekce yukarı getirmek için  
  
#### <a name="to-bring-up-the-type-collection-editor-for-the-send-and-receive-activities"></a>Editor Typu Kolekce yedeklemek için Gönder getirin ve etkinlikleri almak için  
  
1. Seçin **Gönder** veya **alma** Tasarım görünümünde etkinlik.  
  
2. Tuşuna **F4** ortaya çıkarmak için **özellikleri** penceresi.  
  
3. İçinde **özellikleri** penceresinde, yanındaki üç nokta düğmesini tıklatın **KnownTypes** özelliği.  
  
#### <a name="to-bring-up-the-type-collection-editor-for-the-invokemethod-activity"></a>InvokeMethod etkinliği için tür Koleksiyonu Düzenleyicisi'kurmak getirmek için  
  
1. Seçin **InvokeMethod** Tasarım görünümünde etkinlik.  
  
2. Tuşuna **F4** ortaya çıkarmak için **özellikleri** penceresi.  
  
3. İçinde **özellikleri** penceresinde, yanındaki üç nokta düğmesini tıklatın **GenericTypeArguments** özelliği.