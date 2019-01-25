---
title: 'Nasıl yapılır: Bir yönteme parametre eklemek | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], adding a method to a parameter
- Business Data Connectivity service [SharePoint development in Visual Studio], parameter
- BDC [SharePoint development in Visual Studio], adding a method to a parameter
- BDC [SharePoint development in Visual Studio], parameter
- Business Data Connectivity service [SharePoint development in Visual Studio], method parameters
- BDC [SharePoint development in Visual Studio], method parameters
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 0d55c345d9cd0e57d7af2ed359cf4bd9a4f06cd9
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54868124"
---
# <a name="how-to-add-a-parameter-to-a-method"></a>Nasıl yapılır: Bir yönteme bir parametre ekleyin
  Bir parametre bilgileri yönteme geçirmek için veya bir yöntemden bilgi almak için kullanın. Tüm yöntemler, en az bir parametreye sahip olmalıdır. Oluşturmak istediğiniz yöntemi türünü desteklemek için bir parametre tasarlama hakkında daha fazla bilgi için bkz: [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
 Bir yönteme parametre eklemek, Visual Studio model dosyası projenize XML parametre öğesi ekler. Parametre öğesi öznitelikleri hakkında daha fazla bilgi için bkz. [parametre](http://go.microsoft.com/fwlink/?LinkId=169284).  
  
### <a name="to-add-a-parameter-to-a-method"></a>Bir yönteme parametre eklemek için  
  
1.  Bir varlık için bir yöntem ekleyin.  
  
2.  Menü çubuğunda, **görünümü** > **diğer Windows** > **BDC yöntem ayrıntıları**.  
  
     **BDC yöntem ayrıntıları** penceresi açılır. Daha fazla bilgi için [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md).  
  
3.  İçinde **BDC yöntem ayrıntıları** penceresinde yöntemi düğümünü genişletin ve ardından **parametreleri** düğümü.  
  
4.  İçinde **parametre ekleme** listesinde **oluşturma parametresi**.  
  
     Yeni bir parametre altında görünür **parametreleri** düğümü.  
  
5.  Menü çubuğunda, **görünümü** > **Özellikler penceresi**.  
  
6.  İçinde **özellikleri** penceresinde **adı** özelliğini anlamlı bir ad. Örneğin, müşterilerin metodun döndüreceği, yöntemin adını verebilirsiniz **GetCustomers**.  
  
7.  İçinde **BDC yöntem ayrıntıları** penceresinde, parametrenin yönü için görüntülenen listeyi açın ve ardından **içinde**, **Inout**, **kullanıma**, veya **dönüş**.  
  
     Hangi yönde oluşturmakta olduğunuz türü yöntemi için seçme hakkında daha fazla bilgi için bkz. [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
8.  Parametrenin tür tanımlayıcısını değiştirin. Daha fazla bilgi için [nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)   
 [Nasıl yapılır: Modele bir varlık ekleme](../sharepoint/how-to-add-an-entity-to-a-model.md)   
 [Nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)   
 [Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)   
 [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)  
