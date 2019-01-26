---
title: Alan sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: c4de1866-7447-48f7-aa88-28ad92c0b930
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 31370b74405309a3cc67f425da4ce4710031fd70
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54973914"
---
# <a name="space-tab-process-properties-dialog-box"></a>Alan Sekmesi, İşlem Özellikleri İletişim Kutusu
Kullanım **alanı** bir işlemin adres alanı incelemek için sekmesinde. Görüntülenecek [işlem özellikleri iletişim kutusu](../debugger/process-properties-dialog-box.md), odağı Taşı bir [işlemler görünümü](../debugger/processes-view.md) penceresi. Herhangi bir işlem düğümü ağacında seçin ve ardından **özellikleri** gelen **görünümü** menüsü.  
  
 Aşağıdaki ayarlar kullanılabilir **alanı** sekmesinde:  
  
|Giriş|Açıklama|  
|-----------|-----------------|  
|**Alan için işaretlenmişi Göster**|Kategori alanı (görüntü, eşlenmiş, ayrılmış veya atanmamış) seçmek için bu liste kutusunu kullanın.|  
|**Yürütülebilir baytlar**|Seçilen kategori, bu işlemi kullanan tüm adres alanının toplamı. Yürütülebilir bellek programlar tarafından yürütülebilen ancak değil okuma veya yazılan bellektir.|  
|**Çalıştırılabilir-Salt okunur baytlar**|Seçilen kategori için toplam kullanım bu işlemi kullanarak salt okunur özelliklere sahip tüm adres alanında. Çalıştırılabilir-Salt okunur bellek, yürütülen okuma yanı sıra bellektir.|  
|**Çalıştırılabilir-oku-yaz baytları**|Seçilen kategori, bu işlemi kullanarak okuma / yazma özellikleri ile kullanılacak tüm adres alanında toplamı. Çalıştırılabilir-oku yaz, çalıştırılabilen yanı sıra okunabilir ve değiştirilen bellek bellektir.|  
|**Exec-yazma kopyası baytları**|Seçilen kategori, çalıştırılabilen yanı sıra okunabilir ve yazılan tüm adres alanını toplamı. Bu tür işlemler arasında paylaşılan bellek ihtiyacı olduğunda kullanılır. Ardından bunlar paylaşan işlemler bellek salt okunur ise tüm aynı bellek kullanır. Paylaşan bir işlem yazma erişimi isterse, bu bellek kopyasını işlemi yapılır.|  
|**Erişilemez baytlar**|Seçilen kategori için bir işlem kullanmasını engelleyen tüm adres alanının toplamı. Yazma erişimi ihlali oluşturulur veya okuma denenir.|  
|**Salt okunur baytlar**|Seçilen kategori, yürütülen okuma yanı sıra, tüm adres alanının toplamı.|  
|**Oku-yaz baytları**|Seçilen kategori, okuma ve yazma sağlayan tüm adres alanının toplamı.|  
|**Yazma kopyası baytları**|Seçilen kategori için tüm adres alanının toplamı, bellek, okuma yazma için ancak paylaşım sağlar. İşlemler bu bellek okurken, aynı bellek paylaşabilirler. Ancak, paylaşan bir işlem bu paylaşılan bellek, okuma/yazma erişimi istediğinde, yazma için belleğin bir kopyası yapılır.|