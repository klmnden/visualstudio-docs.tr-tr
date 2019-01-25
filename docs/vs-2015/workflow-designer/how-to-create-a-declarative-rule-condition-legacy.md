---
title: 'Nasıl yapılır: Bildirime dayanan Kural koşulu (eski) oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- declarative rule conditions
- condition statements, declarative rule conditions
- Rule Condition Editor dialog box
ms.assetid: 804b6129-c433-408f-a424-46987967730c
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ba2db8f1accafab1bdb20eacab73b2a963391075
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758877"
---
# <a name="how-to-create-a-declarative-rule-condition-legacy"></a>Nasıl yapılır: Bildirime Dayanan Kural Koşulu Oluşturma (Eski)
Bu konu, bir kural koşulu kullanılarak bildirmek açıklar [!INCLUDE[wfd1](../includes/wfd1-md.md)] hedefleyen [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Bir koşul deyimi değerlendiren **True** veya **False**. Bildirime dayanan Kural koşulu kullanılarak oluşturulan bir koşul deyimdir [Kural Koşulu Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-condition-editor-dialog-box-legacy.md) ve sahip iş akışı XML olarak depolanır. İş akışı durumunu ve birden fazla doğrulamaları birleştiren bir Boolean Cebir karşılaştırma doğrulamaları içerebilir.  
  
 Bildirime dayanan kural koşulları aşağıdaki Windows Workflow Foundation out-of-box etkinliklerini kullanılır:  
  
-   [ConditionedActivityGroup](http://go.microsoft.com/fwlink?LinkID=65017)  
  
-   [IfElseBranchActivity](http://go.microsoft.com/fwlink?LinkID=65034)  
  
-   [ReplicatorActivity](http://go.microsoft.com/fwlink?LinkID=65039)  
  
-   [WhileActivity](http://go.microsoft.com/fwlink?LinkID=65049)  
  
-   [SequentialWorkflowActivity](http://go.microsoft.com/fwlink?LinkID=65040)  
  
-   [StateMachineWorkflowActivity](http://go.microsoft.com/fwlink?LinkID=65045)  
  
### <a name="to-create-a-declarative-rule-condition-using-the-rule-condition-editor"></a>Kural Koşulu Düzenleyicisi'ni kullanarak bir bildirime dayanan Kural koşulu oluşturma  
  
1.  Etkinliğin içinde **özellikleri** penceresinde tıklayın **koşul** özelliği veya **UntilCondition** etkinliğe bağlı bir özellik.  
  
2.  Seçin **bildirim temelli bir kural koşulu** özelliği için listeden.  
  
3.  Genişletin **koşul** veya **UntilCondition** özelliği.  
  
4.  Tıklayın **ConditionName** özelliği.  
  
5.  Tıklayın **ConditionName** üç nokta **[...]**  açmak için **koşulu seçin** iletişim kutusu.  
  
6.  Tıklayın **yeni koşul** açmak için **Kural Koşulu Düzenleyicisi** iletişim kutusu.  
  
7.  Koşul ifadesi türü **koşul** metin kutusu.  
  
     Koşul ifadeleri oluşturma hakkında daha fazla bilgi için bkz: [Kural Koşulu Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-condition-editor-dialog-box-legacy.md).  
  
8.  Koşul ifadesi oluşturmayı tamamladığınızda, tıklayın **Tamam** iletişim kutusunu kapatmak ve Kural koşulu ile atanan bir ad oluşturun.  
  
     **Koşulu seçin** iletişim kutusu açılır.  
  
     Nasıl kullanılacağı hakkında daha fazla bilgi için **koşulu seçin** iletişim kutusu, bakın [seçin koşul iletişim kutusu (eski)](../workflow-designer/select-condition-dialog-box-legacy.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski iş akışı etkinlikleri](../workflow-designer/legacy-workflow-activities.md)   
 [ConditionedActivityGroup kullanma](http://go.microsoft.com/fwlink?LinkID=65066)   
 [Öğeye etkinliğini kullanma](http://go.microsoft.com/fwlink?LinkID=65075)   
 [Çoğaltıcı etkinliğini kullanma](http://go.microsoft.com/fwlink?LinkID=65080)   
 [While kullanarak etkinlik](http://go.microsoft.com/fwlink?LinkID=65091)   
 [Kural Koşulu Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-condition-editor-dialog-box-legacy.md)   
 [Koşul seç iletişim kutusu (eski)](../workflow-designer/select-condition-dialog-box-legacy.md)   
 [İş akışlarında koşullar kullanma](http://go.microsoft.com/fwlink?LinkID=65009)