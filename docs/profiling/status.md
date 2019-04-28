---
title: Durum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ba656fa4-ef9d-4d8c-a3b6-739c3b5d23ae
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 25f452dcb473abf87d8992f36f5326973937e85e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967878"
---
# <a name="status"></a>Durum
*VSPerfCmd.exe* **durumu** seçeneği profil oluşturucuyu ve şu anda profillenen herhangi bir işlem durumuyla ilgili bilgileri görüntüler.

 **Durumu** seçeneği, komut satırında belirtilen tek seçenek olması gerekir. Profil Oluşturucu ile başlatılmalıdır *VSPerfCmd.exe* **Başlat** herhangi bir durum görüntülenebilmesi seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Status
```

#### <a name="parameters"></a>Parametreler
 Yok.

## <a name="remarks"></a>Açıklamalar
 **Durumu** seçeneği profil oluşturucu için aşağıdaki durum bilgileri görüntülenir.

 **Çıkış dosya adı** geçerli Profil Oluşturucu veri dosyasının yolu ve dosya adı.

 **Koleksiyon modu** örnek veya izleme

 **En fazla işlem** tek seferde profili işlemlerin sayısı ve şu anda etkin işlem sayısı.

 **En fazla iş parçacığı** tek seferde profili iş parçacığı sayısı.

 **Arabellek sayısı** bellek arabellek sayısı, profil oluşturma veri yazmada ayrılmış.

 **Arabellek boyutu** bellek arabelleğin bayt cinsinden boyutu.

 **Durumu** seçeneği şu anda profili oluşturulan her işlem için aşağıdaki durum bilgileri görüntüler.

 **İşlem** profilli işlemin adı.

 **İşlem Kimliği** işleminin sistem tanımlayıcısı.

 **İş parçacığı sayısı** şu anda çalışan iş parçacıklarının sayısı.

 **Başlat/Durdur sayısını** birincil iç profil oluşturucunun sayımını bu işlem için veri toplamayı denetlemek için. Sayısı, veri toplamak için birine eşit olmalıdır. Başlat/Durdur sayısını gösterilen VSPerfCmd seçenek ve profil oluşturucu API'ler ile yönetilebilir **GlobalOn**, **GlobalOff**, **ProcessOn**, **ProcessOff**, **ThreadOn**, ve **ThreadOff**.

 **Askıya alma/sürdürme sayısı** ikincil iç profil oluşturucunun sayımını bu işlem için veri toplamayı denetlemek için. Sayısı, veri toplamak için sıfıra eşit veya daha az olmalıdır. **Askıya alma/sürdürme** sayısı yalnızca profil oluşturucu tarafından API'leri yönetilebilir.

 **İzleyiciye erişim hakkına sahip kullanıcılar** profil oluşturucu için erişime sahip kullanıcılar adlarını listeler. Ek kullanıcılar verilebilir erişim VSPerfCmd.exe kullanarak **yönetici** seçeneği

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)