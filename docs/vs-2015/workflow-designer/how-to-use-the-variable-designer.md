---
title: 'Nasıl yapılır: Değişken Tasarımcısını kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.View.DesignTimeVariable.UI
ms.assetid: 0318dfb0-bf8f-4f92-9b86-ae4c1b2161ad
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 22096541df20d2eb6ba5bd00c2fc531e9988d5e9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60104297"
---
# <a name="how-to-use-the-variable-designer"></a>Nasıl yapılır: Değişken Tasarımcısını Kullanma
Değişken tasarımcısını kullanmak için değişkenler veri bağlama senaryoları ve koşul deyimlerini oluşturmak için kullanılır. Tasarımcı tıklayarak erişilen **değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Tasarımcı, bir tablo biçiminde görünür ve her bir sütun üst bilgileri dışında sıralanabilir değişkenlerin bir listesi içeren **varsayılan** sütun. Her bir değişken adı, değişken türü, kapsamı ve varsayılan değer (varsa) içerir. Ad ve varsayılan değer düzenlenebilir metin alanları ve türüne ve kapsamına açılan listeler. Kapsam değişken tasarımcısını çağrıldığında, seçilen etkinliğidir. Bir değişken seçimi kapsamında oluşturulamıyorsa, kapsamı en yakın üst etkinliği değişkenleri kapsamında oluşturulmasına izin veren seçimin varsayılacaktır. [!INCLUDE[crabout](../includes/crabout-md.md)] değişkenleri bkz [değişkenleri ve bağımsız değişkenler](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8).  
  
 Sıralama düzenini kullanıcı açıkça sıralama denetimlerden birini kullanır, kapatır ve değişken tasarımcısını yeniden açana veya başka bir değişken oluşturur kadar uygulanmaz.  
  
### <a name="to-create-a-new-variable"></a>Yeni bir değişken oluşturmak için  
  
1. İş akışı veya etkinliği bir çözüm açın [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)].  
  
2. Tasarım tuvalde akışınızda bir etkinlik seçin.  
  
3. Değişken tasarımcısını tıklatarak **değişkenleri** tasarım tuvalin sol alt köşesindeki düğme. Değişken tasarımcısını görünür.  
  
4. Etiketli boş satırı tıklatın **oluşturma değişken**. Bu aşağıdaki varsayılan değerleri kullanarak yeni bir değişken ile yeni bir satır ekler: variablex için **adı** x benzersiz değişken adları oluşturmak için otomatik olarak artırılır 1 başlangıç değeri bir tamsayı olduğu  **Dize** için **değişken türü**, ve **dizisi** için **kapsam**. Hiçbir değer için eklenen **varsayılan**. İş akışı tasarım işlemi sırasında herhangi bir zamanda bu değerleri değiştirebilirsiniz.  
  
    > [!NOTE]
    >  Bir değişkeni silmek için değişken tıklayarak seçin ve tuşuna **Sil** anahtarı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş akışı Tasarımcısını kullanma](../workflow-designer/using-the-workflow-designer.md)   
 [Değişkenler ve bağımsız değişkenler](http://msdn.microsoft.com/library/d03dbe34-5b2e-4f21-8b57-693ee49611b8)   
 [Nasıl yapılır: Bağımsız Değişken Tasarımcısını Kullanma](../workflow-designer/how-to-use-the-argument-designer.md)