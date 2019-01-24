---
title: InvokeDelegate | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- InvokeDelegate Designer
- System.Activities.Statements.InvokeDelegate.UI
ms.assetid: 289a7498-5127-453f-beb5-05f05b80d26f
caps.latest.revision: 3
author: steved0x
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 30281d8cd5d5ed94ed89a980006f9618292a778d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54798913"
---
# <a name="invokedelegate"></a>InvokeDelegate

**InvokeDelegate** Tasarımcısı oluşturmak ve yapılandırmak için kullanılan bir <xref:System.Activities.Statements.InvokeDelegate> etkinlik.

## <a name="the-invokedelegate-activity"></a>InvokeDelegate etkinliği

<xref:System.Activities.Statements.InvokeDelegate> Genel temsilcisini çağırır.

### <a name="using-the-invokedelegate-activity-designer"></a>InvokeDelegate etkinlik Tasarımcısını kullanma

**InvokeDelegate** etkinlik Tasarımcısı bulunabilir **Temelleri** kategorisi **araç kutusu**, hangi erişilen tıklayarak **araçkutusu** sekmesini [!INCLUDE[wfd2](../includes/wfd2-md.md)] (Alternatif olarak, seçin **araç** gelen **görünümü** menü veya CRTL + ALT + X.)

**InvokeDelegate** etkinlik Tasarımcısı, gelen sürüklenebilir **araç kutusu** ve oturum bırakılan [!INCLUDE[wfd2](../includes/wfd2-md.md)] yüzey nerede hiç etkinlikleri genellikle yerleştirilir, gibi olarak içinde bir <xref:System.Activities.Statements.Sequence>. Bu, oluşturur bir <xref:System.Activities.Statements.InvokeDelegate> etkinliği ile bir varsayılan <xref:System.Activities.Activity.DisplayName%2A> InvokeDelegate biri. <xref:System.Activities.Activity.DisplayName%2A> Üst bilgisinde düzenlenebilir **InvokeDelegate** etkinlik Tasarımcısı veya **DisplayName** özellik kılavuzunda kutusu.

### <a name="the-invokedelegate-properties"></a>InvokeDelegate özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.InvokeDelegate> özellikleri Tasarımcısı'nda nasıl kullanıldığı açıklanmaktadır. Bu özellikler, özellik kılavuzunda düzenlenebilir ve bazı şirket düzenlenebilir [!INCLUDE[wfd2](../includes/wfd2-md.md)]Tasarımcı yüzeyine bırakın.

|Özellik Adı|Gerekli|Kullanım|
|-------------------|--------------|-----------|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Kolay adı <xref:System.Activities.Statements.InvokeDelegate> etkinlik. InvokeDelegate varsayılan değerdir.<br /><br /> Ancak <xref:System.Activities.Activity.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.InvokeDelegate.Delegate%2A>|Doğru|Adını <xref:System.Activities.ActivityDelegate> etkinlik yürütüldüğünde çağrılabilir. Bu özellik, Tasarımcı yüzeyinde düzenlenebilir. Bu zorunlu bir özelliğidir.|
|<<xref:System.Activities.Statements.InvokeDelegate.DelegateArguments%2A>|False|Çağrılan temsilci bağımsız değişken koleksiyonu. Anahtarları adlarıdır <xref:System.Activities.DelegateArgument> üzerindeki nesneleri <xref:System.Activities.ActivityDelegate> ve bağımsız değişkenler, ifadeler değerlendirilir ve karşılık gelen atanan değerler <xref:System.Activities.DelegateArgument> nesneleri. Özellik kılavuzunda, üç nokta düğmesini **DelegateArguments** alanını görüntüler **DelegateArguments** iletişim, bu özelliği ayarlayabilirsiniz. Tıklayın **bağımsız değişken oluşturma** bağımsız değişkenleri eklemek için alan.|

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Tanımlama ve iş akışı tasarımcısında etkinlik temsilcileri kullanma](../workflow-designer/how-to-define-and-consume-activity-delegates-in-the-workflow-designer.md)