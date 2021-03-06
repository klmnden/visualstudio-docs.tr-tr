---
title: Sunucu Gezgini'nden Azure sanal makinelere erişen | Microsoft Docs
description: Görüntülemek nasıl bir genel bakış oluşturun ve Azure sanal makinelerini (VM) Visual Studio sunucu Gezgini'ndeki alın.
author: ghogen
manager: jillfra
assetId: eb3afde6-ba90-4308-9ac1-3cc29da4ede0
ms.prod: visual-studio-dev14
ms.technology: vs-azure
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 8/31/2017
ms.author: ghogen
ms.openlocfilehash: 6d6b35218355db686a4154928e5529d213e733d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968034"
---
# <a name="accessing-azure-virtual-machines-from-server-explorer"></a>Sunucu Gezgini'nden Azure Sanal Makineler'e erişme

Azure tarafından barındırılan sanal makineler varsa, sunucu Gezgini'nde erişebilirsiniz. İlk Azure aboneliğinize, mobil hizmetlerinizi görüntülemek için oturum açmanız gerekir. Oturum açmak için sunucu Gezgini'nde Azure düğümü için kısayol menüsünü açın ve seçin **Microsoft Azure'a bağlanma**.

1. Bulut Gezgini'nde bir sanal makine seçin ve ardından, Özellikler penceresini görüntülemek için F4 tuşuna basın.

    Aşağıdaki tablo, hangi özelliklerin kullanılabilir gösterir, ancak tüm salt okunurdur. Bunları değiştirmek için kullanın [Azure portalında](http://go.microsoft.com/fwlink/p/?LinkID=525040).

   | Özellik | Açıklama |
   | --- | --- |
   | DNS adı |Sanal makinenin Internet adresi URL'si. |
   | Ortam |Bir sanal makine için bu özellik her zaman üretim değeridir. |
   | Ad |Sanal makinenin adı. |
   | Boyut |Kullanılabilir bellek ve disk alanı miktarını yansıtır sanal makine boyutu. Daha fazla bilgi için [sanal makine boyutları](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs). |
   | Durum |Değerleri başlatma, Başlarken, durdurma, durduruldu ve durumu alınırken içerir. Durum alınıyor görünürse, geçerli durumu bilinmiyor. Bu özellik için değerleri üzerinde kullanılan değerleri farklı [Azure portalında](http://go.microsoft.com/fwlink/p/?LinkID=525040). |
   | Subscriptionıd |Azure hesabınızda abonelik kimliği. Şirket bu bilgiyi gösterebilirsiniz [Azure portalında](http://go.microsoft.com/fwlink/p/?LinkID=525040) abonelik özelliklerini görüntüleyerek. |
2. Bir uç nokta düğümünü seçin ve ardından görüntülemek **özellikleri** penceresi.
3. Uç nokta kullanılabilir özellikler aşağıdaki tabloda açıklanmaktadır, ancak salt okunurdur. Ekleme veya düzenleme uç noktaları bir sanal makine için kullanmak [Azure portalında](http://go.microsoft.com/fwlink/p/?LinkID=525040). 

   | Özellik | Açıklama |
   | --- | --- |
   | Ad |Uç nokta için bir tanımlayıcı. |
   | Özel bağlantı noktası |Uygulamanız için iç ağ erişimi için bağlantı noktası. |
   | Protokol |Aktarım katmanı Bu uç nokta için kullandığı protokol TCP veya UDP. |
   | Genel bağlantı noktası |Uygulamanızı genel erişim için kullanılan bağlantı noktası. |
