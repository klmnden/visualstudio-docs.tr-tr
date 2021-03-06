---
title: Terminal Hizmetleri aracılığıyla Internet gösterileri 'nı desteklemek için ürün anahtarlarını kullanma | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.date: 07/19/2019
ms.topic: conceptual
description: Terminal Hizmetleri aracılığıyla Internet gösterileri 'nı desteklemek ve RDS erişimini etkinleştirmek için ürün anahtarları kullanmayı öğrenin
ms.openlocfilehash: 19faa64b7eeaebc1b92ca965f686795b31e00e7e
ms.sourcegitcommit: 9fc8b144d4ed1c46aba87c0b7e1d24454e0eea9d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68493376"
---
# <a name="internet-demonstrations-via-terminal-services"></a>Terminal Hizmetleri aracılığıyla Internet gösterileri
Visual Studio aboneliği sayesinde, son kullanıcılara, Terminal Hizmetleri (Windows Server 2003 veya Windows Server 2008) veya Uzak Masaüstü Hizmetleri (Windows Server 2008 R2 ve üzeri) aracılığıyla programlarınızın Internet gösterimlerine erişim izni verebilirsiniz. En fazla 200 anonim kullanıcı, gösteriminizi bu şekilde aynı anda erişebilir. Tanıtımın üretim verilerini kullanmamalıdır. Visual Studio aboneleri, uygulamalarını son kullanıcılara gösterecek şekilde lisanslanır. Terminal Hizmetleri (TS) veya Uzak Masaüstü Hizmetleri (RDS) kullanan bu Internet tanıtımı, Visual Studio aboneliği olmayan son kullanıcıların, yazılımın görsel olarak lisanslanması durumunda tanıtım uygulamasıyla etkileşime girebileceği tek senaryodur. Studio abonelikleri.

Bu, Visual Studio abonelerinin gerektiğinde çok sayıda RDS veya TS bağlantısı kullanabileceği geliştirme ve test haklarına ek niteliğindedir.

## <a name="enabling-rds-access"></a>RDS erişimini etkinleştirme
Visual Studio aboneleri, [abone portalındaki](https://my.visualstudio.com?wt.mc_id=o~msft~docs) [ürün anahtarları](https://my.visualstudio.com/productkeys?wt.mc_id=o~msft~docs) sekmesinde sağlanan bir ürün anahtarı girerek bir Windows sunucusuna erişebilen kullanıcı sayısını artırabilir. Ürün anahtarı almak için ürün anahtarları sayfasına bağlanın ve çalıştırmakta olduğunuz Windows Server sürümüne gidin. "Windows Server < sürümü > R2 Uzak Masaüstü Hizmetleri < Kullanıcı veya cihaz > bağlantıları" ' nı bulun ve **talep anahtarı** bağlantısına tıklayın. Örneğin, Windows Server 2012 R2 üzerinde RDS kullanıyorsanız ve dağıtımınız Kullanıcı Cal 'Lerini kullanıyorsa, "Windows Server 2012 Uzak Masaüstü Hizmetleri Kullanıcı bağlantıları (50)" öğesini seçin.
Her bir türden beş anahtar Windows Server 2008 R2 için kullanılabilir ve her anahtar 20 bağlantıyı destekleyecektir. Windows Server 2012 R2 için, her tür için dört anahtar sağlanır ve her biri 50 bağlantıyı destekleyecektir.

## <a name="to-enable-additional-connections-in-windows-server"></a>Windows Server 'da ek bağlantıları etkinleştirmek için:
1. Sunucu Yöneticisi'ni açın.
2. Sol gezinti bölmesindeki sunucular listesini açın.
3. Lisans sunucunuza sağ tıklayıp "lisansları yüklensin" seçeneğini belirleyin.
4. Sihirbazdaki adımları izleyin.  Anlaşma türünü seçerken, "lisans paketi (Retail)" öğesini seçin ve portaldan aldığınız ürün anahtarını girin.

Son kullanıcılar, aşağıdaki koşullar karşılandığında RDS aracılığıyla uygulamalara erişim sağlayabilir:
- Kullanıcılar anonim (kimliği doğrulanmamış bir durumda) olmalıdır.
- Bağlantılar Internet üzerinden olmalıdır.
- Uygulama gösterileri için 200 adede kadar eşzamanlı kullanıcı bağlantısı kullanılabilir.
- Kullanıcı bağlantılarını etkinleştirmek için ürün anahtarları bir Visual Studio abonesi tarafından alınmalıdır.

## <a name="next-steps"></a>Sonraki adımlar
RDS dağıtımı için yardıma ihtiyacınız varsa, ' de **Uzak Masaüstü Hizmetleri (RDS) 2012 oturum dağıtımında** https://techcommunity.microsoft.com/t5/Ask-The-Performance-Team/bg-p/AskPerf çok parçalı blog serisine göz atın. 

Sorularınız varsa lütfen [Microsoft Uzak Masaüstü Services forumunu](https://social.technet.microsoft.com/Forums/windowsserver/home?forum=winserverTS)ziyaret edin.
