---
title: Genel sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: 86f4d61d-a594-4aac-8960-c5279b4a10fd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6116beb67baf072d9c9762a1e8c67408cc915f29
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62849822"
---
# <a name="general-tab-process-properties-dialog-box"></a>Genel Sekmesi, İşlem Özellikleri İletişim Kutusu
Kullanım **genel** belirli bir işlemle ilgili daha fazla bilgi için sekmesinde. Görüntülenecek [işlem özellikleri iletişim kutusu](../debugger/process-properties-dialog-box.md), odağı Taşı bir [işlemler görünümü](../debugger/processes-view.md) penceresi. Herhangi bir işlem düğümü ağacında seçin ve ardından **özellikleri** gelen **görünümü** menüsü.

 Aşağıdaki ayarlar kullanılabilir **genel** sekmesinde:

|Giriş|Açıklama|
|-----------|-----------------|
|**Modül adı**|Modülün adı.|
|**İşlem kimliği**|Bu işlem benzersiz kimliği. Bunlar işlem ömrü boyunca yalnızca bir işlemi tanımlamak için işlem kimliği numaraları yeniden kullanılır. İşlem nesnesi türü, bir program çalıştırıldığında oluşturulur. Bir işlemdeki tüm iş parçacıkları, aynı adres alanı paylaşabilir ve aynı verilere erişebilir.|
|**Temel öncelik**|Bu işlemin geçerli temel öncelik. Bir işlemdeki iş parçacıkları, yükseltmek ve kendi temel öncelik işlemin temel öncelik göre daha düşük.|
|**İş Parçacıkları**|Bu işlem şu anda etkin iş parçacığı sayısı.|
|**CPU süresi**|Bu işlem ve kendi iş parçacığı üzerinde harcanan toplam CPU süresi. Kullanıcı saati artı ayrıcalıklı zaman eşit.|
|**Kullanıcı Zamanı**|Bu işlemin iş parçacıklarının boşta olmayan iş parçacıklarında kullanıcı modunda kod çalıştırırken harcadığı geçen toplam geçen süre. Alt pencere yöneticisi ve grafik altyapısı gibi gibi uygulamalar kullanıcı modunda yürütün.|
|**Ayrıcalıklı Zaman**|Toplam geçen süre, boş olmayan iş parçacıklarında ayrıcalıklı modda bu işlemin çalıştığı. Hizmet katmanını, başkanlık yordamlar ve çekirdek ayrıcalıklı modunda yürütün. Grafik bağdaştırıcıları ve yazıcılar dışında çoğu cihaz için cihaz sürücüleri ayrıca ayrıcalıklı modda yürütülür. Windows uygulamanız için yaptığı bazı iş ayrıcalıklı zaman yanı sıra diğer alt işlemlerin görünebilir.|
|**Geçen süre**|Bu işlemin çalıştığı toplam geçen süre.|