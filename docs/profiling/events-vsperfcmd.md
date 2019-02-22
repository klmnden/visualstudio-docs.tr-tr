---
title: Olaylar (VSPerfCmd) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: eb139327-4783-4f2a-874c-efad377a7be4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aff97e69b3dea8de9e13c351aa199bc81bdf733c
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56627590"
---
# <a name="events-vsperfcmd"></a>Olaylar (VSPerfCmd)
*VSPerfCmd.exe* **olayları** olay izleme için Windows (ETW) günlüğe kaydetme seçeneği denetler. ETW verilerini Profil Oluşturucu veri dosyasından ayrı .etl dosyasına kaydedilir. Bir raporu kullanarak verileri görüntülenebilir [VSPerfReport](../profiling/vsperfreport.md) /summary:etw komutu.

 **Olayları** seçeneği VSPerfCmd önce herhangi bir zamanda çağrılabilir **kapatma** komutu, profil oluşturmayı durdurmak için çağrılır.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /events {On|Off} {Guid|ProviderName} [,Flags[,Level]
```

#### <a name="parameters"></a>Parametreler
 **Üzerinde**&#124;**kapalı** başlatır veya olay verilerini toplama durur.

 `Guid` Sağlayıcı denetimden GUİD'si.

 `ProviderName` Kayıtlı Windows Yönetim Araçları (WMI) sağlayıcısının adı.

 `Flags` "0 x"-Olay sağlayıcısı tarafından tanımlanan bayrakları onaltılık değer öneki.

 `Level` Toplanan veri miktarını belirtir. `Level` Olay sağlayıcısı tarafından tanımlanır.

 **Olayları** seçeneği sağlayıcı adları olarak aşağıdaki çekirdek anahtar sözcükleri anlar:

 **İşlem** olayları işleme

 **İş parçacığı** olayları için iş parçacığı

 **Görüntü** görüntü yükleme ve kaldırma olayları

 **Disk** Disk g/ç olayları

 **Dosya** dosya g/ç olayları

 **Hardfault** sabit sayfa hataları

 **Pagefault** yazılım sayfa hataları

 **Ağ** ağ olayları

 **Kayıt defteri** kayıt defteri erişimi olayları

 Çekirdek sağlayıcısı yalnızca etkin olduğunu unutmayın. Devre dışı bırakılamaz ya da İzleyici kapatılana dek bayraklarının değiştirilebilir.

## <a name="remarks"></a>Açıklamalar

> [!NOTE]
>  CLR ETW olaylarını etkin olduğunda, ek başlatma verileri de izleme görünümü raporda toplanır. Başlangıç olayları raporda görünmesini dışarıda bırakmak için aşağıdaki komutu kullanın:

```cmd
C:\<path>VSPerfCmd -events on, \".NET Common Language Runtime\", 0x7fffffff, 5
```

> [!IMPORTANT]
>  Başlangıç olayları dışlamazsanız, çünkü bu olaylar Yönetilen Nesne Biçimi (MOF) dosyasında listelenmeyen ardından GUID'leri raporda görünürler. Daha fazla bilgi için Microsoft Web sitesindeki bu sayfaya bakın: [Örnek Yönetilen Nesne Biçimi (MOF) dosyası](http://go.microsoft.com/fwlink/?linkid=37118).

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)