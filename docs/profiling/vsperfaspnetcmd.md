---
title: VSPerfASPNetCmd | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools,VSPerfASPNETCmd
- VSPerfASPNETCmd
ms.assetid: f9e9f895-57bb-41e8-8bd1-cdaa738ec220
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3a6415734a1ea161c7baea26d2abde6d5390ce12
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62581193"
---
# <a name="vsperfaspnetcmd"></a>VSPerfASPNetCmd
**VSPerfASPNetCmd.exe** komut satırı aracı sayesinde profili ASP.Net web sitelerine gerektirmeden ortam değişkenlerini ayarlama veya bilgisayarınızı yeniden başlatın. Kullanım **VSPerfASPNetCmd.exe** yerine [VSPerfCmd](../profiling/vsperfcmd.md) ne zaman, ASP.NET Web sitesini profil ve tarafından sağlanan ek işlevsellik gerekmeyen **VSPerfCmd**. Hakkında daha fazla bilgi için **VSPerfASPNetCmd**, bkz: [VSPerfASPNETCmd ile hızlı web sitesi profili oluşturma](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md). **VSPerfASPNetCmd** bağımsız profil oluşturucuyu bir ASP.NET web sitesinin profilini çıkarmak için kullanırken kullanmak için tercih edilen komut satırı aracıdır.

## <a name="syntax"></a>Sözdizimi
 **vsperfaspnetcmd** [/*seçenekleri*] *Web sitesi*

## <a name="options"></a>Seçenekler

|Seçenek|Açıklama|
|------------|-----------------|
|**/ Örnek** veya **/s**|Örnekleme metodu kullanılarak profilleri Web sitesi. **/ Örnek** için varsayılan yöntemdir. / Örnek ile birlikte kullanılamaz **/Trace**.|
|**/ İzleme** veya **/t**|Araçlar yöntemini kullanarak profilleri Web sitesi. / İzleme ile birlikte kullanılamaz **/Sample**.|
|**/ Bellek**[**:**`Type`] veya **/m**[**:**{**bir**&#124;**l**}]|Bellek ayırma profilini oluşturur ve isteğe bağlı olarak, nesne kullanım ömrü (atık toplama) profilleri. **/ Bellek** örnekleme veya araç haline getirme yöntemi ile kullanılabilir.<br /><br /> *Tür* aşağıdakilerden biri olabilir:<br /><br /> -   **ayırma** (veya **bir**) yalnızca bellek ayırma verileri toplar.<br />-   **yaşam süresi** (veya **l**) bellek ayırma ve nesne yaşam süresi verisi toplar.<br /><br /> Varsayılan `Type` olduğu **ayırma**.|
|**/ İpucu** veya **/i**|Profil oluşturma verileri ayrıntılı ASP.NET isteğinin ve ADO.NET çağrı bilgilerini ekler. **/ İpucu** örnekleme veya araç haline getirme yöntemi ile kullanılabilir ve ile kullanılabilir **/Memory** seçeneği.|
|**Çıkış:** `File` veya   **/o:**`File`|Profil oluşturma veri yolu ve dosya adını belirtir (. *Vsp*) dosyası.|
|**/ NoWait** veya **/n**|Ek komutlar komut istemi penceresinde kullanılabilir böylece komut hemen sor döndürür. Yazmanız gerekir **VSPerfASPNETCmd/shutdown** profil oluşturma devre dışı bırakmak için ayrı bir komut satırında.|
|**/ PackSymbols**[: {**üzerinde**&#124;**kapalı**} veya **/p**[: {**üzerinde**&#124;**Kapalı**}|Semboller (işlev ve parametre adları, vb.), profil oluşturma verilerini katıştırır (. *Vsp*) dosyası.|
|**/ Shutdown:** `Website`veya   **/d:**`Website`|Profil oluşturma kapatır. Kullandıktan sonra bir komut satırında tek seçenek olarak kullanın **/nowait** profil oluşturma, başlatmak için seçeneği veya profil oluşturucuyu beklenmedik şekilde sona erer. Özgün kullandığınız aynı URL'yi belirtin **VSPerfASPNETCmd** komutu.|
|`Website`|Profili oluşturulacak Web sitesi URL'si.|

## <a name="see-also"></a>Ayrıca bkz.
- [Profil oluşturma VSPerfASPNETCmd ile hızlı web sitesi](../profiling/rapid-web-site-profiling-with-vsperfaspnetcmd.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
