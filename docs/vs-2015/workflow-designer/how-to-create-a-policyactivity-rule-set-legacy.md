---
title: 'Nasıl yapılır: (Eski) PolicyActivity kural kümesi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- PolicyActivity activity, creating rule sets
- Rule Set Editor dialog box
- PolicyActivity activity, selecting rule sets
- Select Rule Set dialog box
- rule sets, creating for PolicyActivity
ms.assetid: f272489d-3342-4511-8b59-6a0fd7a42d70
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5e7528e8a589cb64e4debc8c1e119f8f59a6244c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54766609"
---
# <a name="how-to-create-a-policyactivity-rule-set-legacy"></a>Nasıl yapılır: PolicyActivity Kural Kümesi Oluşturma (Eski)
Bu konu eski kullanılarak ayarlanan ilke etkinlik kuralının nasıl oluşturulacağını açıklar [!INCLUDE[wfd1](../includes/wfd1-md.md)] hedefleyen [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Sürüklenen sonra bir **ilke** etkinlik öğesinden **araç kutusu** iş akışı tasarım yüzeyine, mevcut bir kuralı seçin veya yeni bir kural kümesini oluşturmak isteyeceksiniz [PolicyActivity ](http://go.microsoft.com/fwlink?LinkID=65019) etkinlik. Mevcut bir kuralı ayarlamak için seçtiğiniz [seçin kuralı Ayarla iletişim kutusu (eski)](../workflow-designer/select-rule-set-dialog-box-legacy.md) ve kullanarak kural kümeleri oluşturma [kural kümesi Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-set-editor-dialog-box-legacy.md).  
  
> [!NOTE]
>  Açabileceğiniz [kural kümesi Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-set-editor-dialog-box-legacy.md) doğrudan çift tıklatarak iletişim kutusunu bir [PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019) iş akışı tasarım yüzeyinde etkinlik.  
  
### <a name="to-select-or-create-a-rule-set-for-a-policyactivity-activity"></a>Seçmek veya PolicyActivity etkinliği için bir kural oluşturmak için  
  
1.  Sağ [PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)ve ardından **özellikleri** açmak için **özellikleri** penceresi.  
  
2.  Tıklayın **RuleSetReference** özelliği.  
  
3.  Aşağıdakilerden birini yapın:  
  
    -   Tıklayın **RuleSetReference** üç nokta **[...]** seçip kümesinde mevcut bir kuralı [seçin kuralı Ayarla iletişim kutusu (eski)](../workflow-designer/select-rule-set-dialog-box-legacy.md). Ardından 10. adıma gidin.  
  
         -veya-  
  
    -   Bir kural kümesi için bir ad yazın. Tıklayın **RuleSetReference** üç nokta **[...]** ve ardından **Düzenle** içinde [seçin kuralı Ayarla iletişim kutusu (eski)](../workflow-designer/select-rule-set-dialog-box-legacy.md).  
  
         -veya-  
  
    -   Bir kural kümesi için bir ad yazın. Genişletin **RuleSetReference** özelliği ve üç noktayı seçin **[...]**  içinde **RuleSet tanımı** özelliği.  
  
         [Kural kümesi Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-set-editor-dialog-box-legacy.md) açılır.  
  
4.  İçinde [kural kümesi Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-set-editor-dialog-box-legacy.md), tıklayın **Kuralı Ekle** kural kümesine yeni bir kural eklemek için.  
  
5.  Girin **adı**, **öncelik**, ve **yeniden değerlendirme** özellikleri veya varsayılan değerleri koruyun.  
  
6.  Metni girin **koşul**.  
  
7.  Metni girin **ardından Eylemler** ve **başka eylemler**.  
  
8.  Tıklayın **Kuralı Ekle** yeniden başka bir kural eklemek için.  
  
9. İşiniz bittiğinde **Tamam**'a tıklayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [PolicyActivity](http://go.microsoft.com/fwlink?LinkID=65019)   
 [Select kuralı Ayarla iletişim kutusu (eski)](../workflow-designer/select-rule-set-dialog-box-legacy.md)   
 [Kural kümesi Düzenleyicisi iletişim kutusu (eski)](../workflow-designer/rule-set-editor-dialog-box-legacy.md)   
 [İlke etkinliği kullanma](http://go.microsoft.com/fwlink?LinkID=65004)   
 [Eski İş Akışı Etkinlikleri ](../workflow-designer/legacy-workflow-activities.md)