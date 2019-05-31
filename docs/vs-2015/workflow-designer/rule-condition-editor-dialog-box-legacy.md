---
title: Kural Koşulu Düzenleyicisi iletişim kutusu (eski) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Workflow.Activities.Rules.Design.RuleConditionDialog.UI
helpviewer_keywords:
- Rule Condition dialog box
ms.assetid: c7ca8be9-de31-4a64-939c-4d53a50d5e29
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8237c8e29007d010cd99e4323bf8e88a23b7e9fb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63006833"
---
# <a name="rule-condition-editor-dialog-box-legacy"></a>Kural Koşulu Düzenleyicisi İletişim Kutusu (Eski)
Bu konu açıklar nasıl **Kural Koşulu Düzenleyicisi** eski iletişim kutusunda [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Eski kullanın [!INCLUDE[wfd2](../includes/wfd2-md.md)] hedeflemek gerektiğinde [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Kullanarak bildirim temelli bir kural koşulları oluşturup **Kural Koşulu Düzenleyicisi** iletişim kutusu. Bu kural koşulları, aşağıdaki Windows Workflow Foundation out-of-box etkinlikleri özellikleri olarak sunulur:  
  
- [ConditionedActivityGroup](http://go.microsoft.com/fwlink?LinkID=65017)  
  
- [IfElseBranchActivity](http://go.microsoft.com/fwlink?LinkID=65034)  
  
- [ReplicatorActivity](http://go.microsoft.com/fwlink?LinkID=65039)  
  
- [WhileActivity](http://go.microsoft.com/fwlink?LinkID=65049)  
  
- [SequentialWorkflowActivity](http://go.microsoft.com/fwlink?LinkID=65040)  
  
- [StateMachineWorkflowActivity](http://go.microsoft.com/fwlink?LinkID=65045)  
  
  Size erişim **Kural Koşulu Düzenleyicisi** iletişim kutusunu kullanarak [seçin koşul iletişim kutusu (eski)](../workflow-designer/select-condition-dialog-box-legacy.md).  
  
  Aşağıdaki tabloda kullanıcı arabirimi (UI) öğelerini açıklar **Kural Koşulu Düzenleyicisi** iletişim kutusu.  
  
|Arabirim Öğesi|Açıklama|  
|----------------|-----------------|  
|**Koşul:**|Kural koşulu için ifade girin.|  
|**TAMAM**|Kural koşulu kaydetmek için tıklatın.|  
  
## <a name="entering-condition-expressions"></a>Koşul ifadeleri girme  
 Koşul ifadeleri, metin olarak girilir. Yazabilirsiniz **bu.** alanlar, özellikler ve iş akışında kullanılan yöntemleri başvurmak için düzenleyicide yerleşik bir IntelliSense benzeri menüsünü kullanarak. Veya doğrudan bir iş akışı üye adı yazın. Mantıksal işleçler AND, OR'gibi bir koşul ekleyebilirsiniz ve değil. Koşullar da ekleyebilirsiniz. Bir ikili işleç ve iki işlenenden koşuldur. Desteklenen ikili işleçler **==** , **>** , **\<** , **>=** , ve **<=** . Desteklenen işlenenler şunlardır: sabit değer, aritmetik işlevi ve kapsamlı bir genel üyeler.  
  
 Karşılaştırma türü belirtebilir ve'karşılaştırabilirsiniz **null** ya da boş bir dize. Örneğin, bir karmaşık tür içeren bir değişken üzerinde iç içe geçmiş çağrıları üyelerine yapabileceğiniz `this.Address.State == "WA"`.  
  
 Kural Koşulu Düzenleyicisi aşağıdaki işleçleri destekler:  
  
- İlişkisel işleçleri: ==, =,! =  
  
- Karşılaştırma işleçleri: <, \<=, >, > =  
  
- Aritmetik işleçler: +, -, *, /, MOD  
  
- Mantıksal işleçler: VE &AMP; &AMP;, OR &AMP;#124; &AMP;#124;DEĞİL,!  
  
- Bit düzeyinde işleçler: &,&#124;  
  
  İfadenin İşleç önceliği, C# İşleç önceliği kurallarını izler.  
  
  Kural Koşulu Düzenleyicisi aşağıdaki sayısal ifadeler destekler:  
  
  this.i == 1 D (1.0 çözümler)  
  
  this.i 1E1 == (10.0 için çözümler)  
  
  this.i == 1 L (çözümler uzun olarak)  
  
  this.i == 1 M (ondalık olarak çözümler)  
  
  this.i 1F == (tek bir çözümler)  
  
  this.i 1U == (bir'unsigned int çözümler)  
  
  Koşullar hakkında daha fazla bilgi için bkz. [iş akışlarını kullanarak koşullarında](http://go.microsoft.com/fwlink?LinkID=65009).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IfElseActivity](http://go.microsoft.com/fwlink?LinkID=65033)   
 [ConditionedActivityGroup](http://go.microsoft.com/fwlink?LinkID=65017)   
 [ReplicatorActivity](http://go.microsoft.com/fwlink?LinkID=65039)   
 [WhileActivity](http://go.microsoft.com/fwlink?LinkID=65049)   
 [Koşul seç iletişim kutusu (eski)](../workflow-designer/select-condition-dialog-box-legacy.md)   
 [İş akışlarında koşullar kullanma](http://go.microsoft.com/fwlink?LinkID=65009)   
 [Windows Workflow Foundation Kullanıcı Arabirimi Yardımı için Eski Tasarımcı](../workflow-designer/legacy-designer-for-windows-workflow-foundation-ui-help.md)