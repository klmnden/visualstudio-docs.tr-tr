---
title: Sayfa dosyası sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: daf41a06-8a55-48f6-95f5-49a8416bd308
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d45fa813a7bb75ea0cdd11a412ae35e5444883dc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54924973"
---
# <a name="page-file-tab-process-properties-dialog-box"></a>Sayfa Dosyası Sekmesi, İşlem Özellikleri İletişim Kutusu
Kullanım **sayfa dosyası** işleminin disk belleği dosyasını incelemek için sekmesinde. Görüntülenecek [işlem özellikleri iletişim kutusu](../debugger/process-properties-dialog-box.md), odağı Taşı bir [işlemler görünümü](../debugger/processes-view.md) penceresi. Herhangi bir işlem düğümü ağacında seçin ve ardından **özellikleri** gelen **görünümü** menüsü.  
  
 Aşağıdaki ayarlar kullanılabilir **sayfa dosyası** sekmesinde:  
  
|Giriş|Açıklama|  
|-----------|-----------------|  
|**Sayfa dosyası baytları**|Bu işlem, disk belleği dosyasını kullanarak sayfa geçerli sayısı. Disk belleği dosyası, sayfa işlemi tarafından kullanılan, ancak diğer dosyaları bulunmayan veri depolar. Disk belleği dosyası tüm işlemler tarafından kullanılır ve diğer işlemleri çalışırken yetersiz disk belleği dosyasında alan, hatalara neden olabilir.|  
|**Tepedeki sayfa dosyası baytları**|Bu işlem disk belleği dosyasında kullanılan sayfa sayısı.|  
|**Sayfa hataları**|Bu işlemde çalışan iş parçacığı tarafından sayfa hataları sayısı. Bir iş parçacığı çalışma ana belleğe kümesinde olmayan bir sanal bellek sayfa başvurduğunda bir sayfa hatası oluşur. Bekleme listesinde ise, bu nedenle, sayfa diskten alınmayacak ve bu nedenle zaten bellekte ana ya da bunu bir başkası tarafından kullanılıp kullanılmadığını işlemek sayfa paylaşılan ile.|