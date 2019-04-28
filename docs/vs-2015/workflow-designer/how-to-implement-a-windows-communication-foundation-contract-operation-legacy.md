---
title: 'Nasıl yapılır: Bir Windows Communication Foundation sözleşme işlemi (eski) uygulayan | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: d6aeb20e-fac8-4a9d-bd26-ae78bef96b41
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 56866e084eac7dc3a3ac2a0b80baaa2533ccd285
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62931197"
---
# <a name="how-to-implement-a-windows-communication-foundation-contract-operation-legacy"></a>Nasıl yapılır: Windows Communication Foundation Sözleşme İşlemi Uygulama (Eski)
Bu konu nasıl uygulanacağını açıklar bir [!INCLUDE[indigo1](../includes/indigo1-md.md)] sözleşme işlemi kullanılarak [!INCLUDE[wfd1](../includes/wfd1-md.md)] hedefleyen [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Sürükleme sonra bir **ReceiveActivity** iş akışı tasarım yüzeyine etkinliğini araç kutusundan ya da oluşturduğunuz yeni bir [!INCLUDE[indigo2](../includes/indigo2-md.md)] sözleşme veya var olan bir sözleşmeyi almak ve işlemleri uygular. Seçin ve/veya anlaşmanızda oluşturup aracılığıyla işlemlerini [seçin işlemi iletişim kutusu (eski)](../workflow-designer/choose-operation-dialog-box-legacy.md).  
  
### <a name="to-implement-a-wcf-contract-operation"></a>Bir WCF sözleşmesi işlemini uygulamak için  
  
1. Çift **ReceiveActivity** etkinlik Tasarımcısı'nda veya yanındaki üç noktaya tıklayın **ServiceOperationInfo** özelliğinde **özellikleri** bölmesi.  
  
2. Aşağıdakilerden birini yapın:  
  
   - Tıklayın **ekleme Sözleşme** iletişim kutusunun sağ alt köşesindeki. Bu yeni bir oluşturur [!INCLUDE[indigo2](../includes/indigo2-md.md)] sözleşme ve sizin için işlem.  
  
      -veya-  
  
   - Tıklayın **alma** iletişim kutusunun sağ alt köşesindeki. [Göz atın ve bir .NET türünü seç iletişim kutusu (eski)](../workflow-designer/browse-and-select-a-dotnet-type-dialog-box-legacy.md) açılır. Bir derleme veya istediğiniz sözleşme içeren proje arayın. Sözleşme seçin ve tıklayın **Tamam**.  
  
     Bir sözleşme oluşturulan veya içeri sonra oluşturulan veya içeri aktarılan anlaşması için yeni işlemleri ekleyebilirsiniz. Yeni işlem eklemek, sözleşmeyi seçin ve **ekleme işlemi** iletişim kutusunun sağ alt köşesindeki. Ekleme işlemleri tamamladığınızda, 3. adıma geçin.  
  
3. İle ilişkilendirmek istediğiniz işlemi seçin **ReceiveActivity** etkinlik. İşlemi tanımı, işlem adı, parametreleri, özellikleri ve izin ayarlarını değiştirerek değiştirebilirsiniz.  
  
    Adı değiştirmek için yeni adı girin. **işlem adı** metin kutusu.  
  
    Tıklayın **parametreleri** işlemin parametrelerinin erişmek için sekmesinde. Adı, türü veya parametre yönünü değiştirme yanı sıra ekleyebilir veya işlemi parametreleri silebilirsiniz.  
  
    Tıklayın **özellikleri** işlemin işlem koruma düzeyi ve desteklenen ileti exchange işlevine erişmek için sekmesinde.  
  
    Tıklayın **izinleri** işlemini uygulamak için hangi grupları izin verildiğini belirtmek için sekmesinde.  
  
4. Tıklayın **Tamam** ve **ReceiveActivity** etkinlik, işlem adı uyguladığı işlemi için görüntülenir.  
  
5. Bu işlem içinde uygulanması için kullanılacak seçeceğiz iş akışı etkinliklerin **ReceiveActivity** etkinlik.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İşlem iletişim kutusu (eski) seçin](../workflow-designer/choose-operation-dialog-box-legacy.md)   
 [Nasıl yapılır: Bir WCF sözleşmesi işlemi (eski) Çağır](../workflow-designer/how-to-invoke-a-windows-communication-foundation-contract-operation-legacy.md)   
 [Eski İş Akışı Etkinlikleri ](../workflow-designer/legacy-workflow-activities.md)