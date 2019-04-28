---
title: Sayfa dosyası sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: daf41a06-8a55-48f6-95f5-49a8416bd308
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 25dc3b0aca1b58c18ae4038540c14fc4dbfe4036
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62904113"
---
# <a name="page-file-tab-process-properties-dialog-box"></a>Sayfa Dosyası Sekmesi, İşlem Özellikleri İletişim Kutusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kullanım **sayfa dosyası** işleminin disk belleği dosyasını incelemek için sekmesinde. Görüntülenecek [işlem özellikleri iletişim kutusu](../debugger/process-properties-dialog-box.md), odağı Taşı bir [işlemler görünümü](../debugger/processes-view.md) penceresi. Herhangi bir işlem düğümü ağacında seçin ve ardından **özellikleri** gelen **görünümü** menüsü.  
  
 Aşağıdaki ayarlar kullanılabilir **sayfa dosyası** sekmesinde:  
  
|Giriş|Açıklama|  
|-----------|-----------------|  
|**Sayfa dosyası baytları**|Bu işlem, disk belleği dosyasını kullanarak sayfa geçerli sayısı. Disk belleği dosyası, sayfa işlemi tarafından kullanılan, ancak diğer dosyaları bulunmayan veri depolar. Disk belleği dosyası tüm işlemler tarafından kullanılır ve diğer işlemleri çalışırken yetersiz disk belleği dosyasında alan, hatalara neden olabilir.|  
|**Tepedeki sayfa dosyası baytları**|Bu işlem disk belleği dosyasında kullanılan sayfa sayısı.|  
|**Sayfa hataları**|Bu işlemde çalışan iş parçacığı tarafından sayfa hataları sayısı. Bir iş parçacığı çalışma ana belleğe kümesinde olmayan bir sanal bellek sayfa başvurduğunda bir sayfa hatası oluşur. Bekleme listesinde ise, bu nedenle, sayfa diskten alınmayacak ve bu nedenle zaten bellekte ana ya da bunu bir başkası tarafından kullanılıp kullanılmadığını işlemek sayfa paylaşılan ile.|
