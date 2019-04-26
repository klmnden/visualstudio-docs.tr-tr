---
title: Azure hata ayıklama seçenekleri, bulut Hizmetleri | Microsoft Docs
description: Azure bulut hizmetlerinde hata ayıklama
services: visual-studio-online
documentationcenter: n/a
author: mikejo
manager: douge
editor: ''
ms.assetid: 80755da7-8350-4f5c-97ce-2962beabb36d
ms.service: visual-studio-online
ms.devlang: multiple
ms.topic: article
ms.tgt_pltfrm: multiple
ms.workload: na
origin.date: 03/18/2017
ms.date: 05/11/2018
ms.author: v-junlch
ms.openlocfilehash: 3ec6778f7244df7ad535da066d8e0d91d8c0671e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62560733"
---
# <a name="learn-the-various-ways-to-debug-an-azure-cloud-service"></a>Azure bulut hizmetinde hata ayıklamanın çeşitli yöntemlerini öğrenme
Bu makalede, Azure bulut hizmeti hata ayıklamak için çeşitli yollar için bağlantılar sağlar. 

## <a name="debugging-an-azure-cloud-service-in-visual-studio"></a>Azure bulut hizmetinde Visual Studio'da hata ayıklama
Zamandan tasarruf edebilirsiniz ve Azure kullanarak para işlem bulut hizmetinizi yerel bir makinede hata ayıklamak için öykünücü. Dağıtmadan önce bir hizmet yerel olarak hata ayıklama tarafından güvenilirlik ve performans işlem süresi için ödeme yapmadan artırabilir. Azure'da bir bulut hizmeti çalıştırdığınızda, ancak bazı hatalar meydana gelebilir. Hizmetinizi yayımladığınızda, uzaktan hata ayıklama ve ardından bir rol örneği için Haya ayıklayıcı sağlayarak yalnızca bir bulut hizmeti Azure'da çalıştırdığınızda oluşan hataları ayıklanabilir. Daha fazla bilgi için [yerel bilgisayarınızda, bir bulut hizmetinde hata ayıklama](vs-azure-tools-debug-cloud-services-virtual-machines.md#debug-your-cloud-service-on-your-local-computer).

## <a name="using-intellitrace"></a>IntelliTrace’i kullanma 
Rolleri hedeflenen .NET Framework 4.5 yazmak için Visual Studio Enterprise'ı kullanıyorsanız, IntelliTrace Visual Studio'dan Azure bulut hizmeti dağıtma zaman etkinleştirebilirsiniz. IntelliTrace, Visual Studio ile Azure'da çalışıyormuş gibi uygulamanızda hata ayıklamak için kullanabileceğiniz bir günlük sağlar. Daha fazla bilgi için [IntelliTrace ve Visual Studio ile yayımlanan bulut hizmeti hata ayıklama](http://go.microsoft.com/fwlink/p/?LinkId=623016).

## <a name="remote-debugging"></a>Uzaktan hata ayıklama 
Uzaktan bulut hizmetlerinizi Visual Studio'dan bulut hizmeti dağıtırken zamanında hata ayıklamayı etkinleştirebilirsiniz. Bir dağıtım için uzaktan hata ayıklama etkinleştirmeyi seçerseniz, uzaktan hata ayıklama hizmetleri her rol örneğini çalıştıran sanal makinelere yüklenir. Gibi bu hizmetler - `msvsmon.exe` - performans etkilemez ya neden ek maliyetler. Daha fazla bilgi için [Azure bulut hizmetinde hata ayıklama](vs-azure-tools-debug-cloud-services-virtual-machines.md#debug-a-cloud-service-in-azure).

## <a name="next-steps"></a>Sonraki adımlar
- [Bir Azure bulut hizmeti veya VM Visual Studio'da hata ayıklama](./vs-azure-tools-debug-cloud-services-virtual-machines.md) -Azure bulut hizmetlerinde hata ayıklama konusunda ayrıntılı bilgi edinin.

<!-- Update_Description: update metedata properties -->