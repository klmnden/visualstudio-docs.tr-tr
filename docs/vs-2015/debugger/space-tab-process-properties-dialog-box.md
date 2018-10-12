---
title: Alan sekmesi, işlem özellikleri iletişim kutusu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: c4de1866-7447-48f7-aa88-28ad92c0b930
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 03b73263f6db5e702a44b8854517ec5ee132b561
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49259928"
---
# <a name="space-tab-process-properties-dialog-box"></a>Alan Sekmesi, İşlem Özellikleri İletişim Kutusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

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



