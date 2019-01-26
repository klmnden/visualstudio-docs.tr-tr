---
title: İş Akışı Tasarımcısı - State etkinlik Tasarımcısı
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.State.UI
ms.assetid: 9455ab37-93a0-4c46-9eb8-b6611ca23167
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 2d69b5533ebaf617563c7ce8ff9ba83453bc2fb0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54926156"
---
# <a name="state-activity-designer"></a>State Etkinlik Tasarımcısı

A <xref:System.Activities.Statements.State> içinde bir Durum makinesi olabilir bir durumu temsil eder.

## <a name="using-the-state-activity-designer"></a>State etkinlik Tasarımcısı'nı kullanarak

Eklemek için bir <xref:System.Activities.Statements.State> bir iş akışına sürükleyin **durumu** etkinlik Tasarımcısı'ndan **Durum makinesi** bölümünü **araç kutusu** oturum bırakın bir <xref:System.Activities.Statements.StateMachine> İş Akışı Tasarımcısı yüzeyine etkinliği. A <xref:System.Activities.Statements.State> etkinlik bırakılan üzerine bir <xref:System.Activities.Statements.StateMachine> ve geçişleri eklenen daha sonra; veya bir geçiş olarak oluşturulabilir <xref:System.Activities.Statements.State> etkinlik bırakıldı. Eklemek için bir <xref:System.Activities.Statements.State> etkinliği ve bir geçiş tek adımda Sürükle oluşturmak bir **durumu** etkinliğinden **Durum makinesi** bölümünü **araç kutusu** ve başka gelin İş akışı tasarımcısında durumu. Zaman sürüklenen <xref:System.Activities.Statements.State> başka bir özelliktir <xref:System.Activities.Statements.State>, dört üçgenler diğer görünür <xref:System.Activities.Statements.State>. Varsa <xref:System.Activities.Statements.State> bırakılan dört üçgenler birini durumu makineye eklenir ve bir geçiş kaynak sunucudan oluşturulan <xref:System.Activities.Statements.State> bırakılan hedefe <xref:System.Activities.Statements.State>. Daha fazla bilgi için [geçiş](../workflow-designer/transition-activity-designer.md).

### <a name="state-activity-properties-in-the-workflow-designer"></a>İş akışı tasarımcısında State etkinlik özellikleri

Aşağıdaki tabloda <xref:System.Activities.Statements.State> iş akışı Tasarımcısı'nı kullanarak ayarlanabilir ve Tasarımcısı'nda nasıl kullanıldığını açıklar. Bu özelliklerin bazıları özellik kılavuzunda düzenlenebilir ve bazı Tasarımcı yüzeyinde düzenlenebilir.

|Özellik Adı|Gerekli|Kullanım|
|-|--------------|-|
|<xref:System.Activities.Statements.State.DisplayName%2A>|False|Kolay adı belirtir <xref:System.Activities.Statements.State> üst bilgisindeki etkinlik Tasarımcısı. Varsayılan değer **durumu**. Değer özellik kılavuzunda veya etkinlik Tasarımcısı başlığındaki doğrudan düzenleyebilirsiniz. <xref:System.Activities.Statements.State.DisplayName%2A> İş akışı Tasarımcısı üst kısmında görüntülenen içerik haritalı gezinme kullanılır.<br /><br /> Ancak <xref:System.Activities.Statements.State.DisplayName%2A> kati şekilde gerekli değil kullanmak için en iyi bir uygulamadır.|
|<xref:System.Activities.Statements.State.Entry%2A>|False|Bu durum için geçirildiğinde basıldığında uygulanacak eylemi belirtir. Zaman <xref:System.Activities.Statements.State> etkinlik genişletilir, bu değer, bir etkinlikten sürükleyerek ayarlanabilir **araç kutusu** üzerine sürükleyip bırakarak **giriş** durumu bölümü.|
|<xref:System.Activities.Statements.State.Exit%2A>|False|Bu durum, liste kutusundan geçirildiğinde basıldığında uygulanacak eylemi belirtir. Zaman <xref:System.Activities.Statements.State> etkinlik genişletilir, bu değer, bir etkinlikten sürükleyerek ayarlanabilir **araç kutusu** üzerine sürükleyip bırakarak **çıkış** durumu bölümü.|
|<xref:System.Activities.Statements.State.Transitions%2A>|False|Kaynaklanan olası geçişler listeler <xref:System.Activities.Statements.State>. Listedeki her öğeye olan ilişkili bağlantı <xref:System.Activities.Statements.Transition> ve hedef <xref:System.Activities.Statements.State>. Bağlantı tıklatıldığında geçirir Tasarımcı için Genişletilmiş görünümde <xref:System.Activities.Statements.Transition> veya <xref:System.Activities.Statements.State>.|

## <a name="see-also"></a>Ayrıca bkz.

- [StateMachine](../workflow-designer/statemachine-activity-designer.md)
- [FinalState](../workflow-designer/finalstate-activity-designer.md)
- [Transition](../workflow-designer/transition-activity-designer.md)