---
title: 'Nasıl yapılır: Metot örneği tanımlama | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], method instance
- BDC [SharePoint development in Visual Studio], method instance
- BDC [SharePoint development in Visual Studio], method
- Business Data Connectivity service [SharePoint development in Visual Studio], method
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 318744ec1a1a9214ce0385fc56fb1c0cf340339b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62814117"
---
# <a name="how-to-define-a-method-instance"></a>Nasıl yapılır: Metot örneği tanımlama
  Her yöntem için en az bir metot örneği modelinizde tanımlamanız gerekir.

 Kullanarak bir metot örneği Ekle **BDC yöntem ayrıntıları** penceresi. Metot örneği eklediğinizde, Visual Studio ekler bir `<MethodInstance>` model dosyası projenize XML öğesi. Öznitelikleri hakkında daha fazla bilgi için bir `<MethodInstance>` öğesi bkz [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282).

### <a name="to-define-a-method-instance"></a>Metot örneği tanımlamak için

1. İçinde **BDC yöntem ayrıntıları** penceresinde bir yöntemin düğümünü genişletin ve ardından **örnekleri** düğümü.

2. İçinde **metot örneği Ekle** listesinde **Bulucu örneği oluştur**.

     Yeni metot örneği altında görünür **örnekleri** düğümü.

3. Menü çubuğunda, **görünümü** > **Özellikler penceresi**.

4. İçinde **özellikleri** penceresinde metot örneği özelliklerini ayarlayın. Her bir özellik hakkında daha fazla bilgi için bkz: [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282).

## <a name="see-also"></a>Ayrıca bkz.
- [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)
- [Nasıl yapılır: Modele bir varlık ekleme](../sharepoint/how-to-add-an-entity-to-a-model.md)
- [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)
- [Nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)
- [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)
