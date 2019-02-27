---
title: 64 Bit uygulamalarda hata ayıklama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], 64-bit
- 64-bit debugging
ms.assetid: db648e5f-6375-4e2d-aa98-eb7261958927
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 206b14a1cdab61d64354e134449149b70a030683
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/27/2019
ms.locfileid: "56954499"
---
# <a name="debug-64-bit-applications"></a>64 Bit uygulamalarda hata ayıklama
Yerel bilgisayarda veya uzak bilgisayarda çalışan bir 64-bit uygulamada hata ayıklaması yapabilirsiniz.

 Bir uzak bilgisayarda çalışan 64-bit bir uygulamada hata ayıklamak için bkz: [uzaktan hata ayıklama](../debugger/remote-debugging.md).

 64 bit uygulamalarda hata ayıklama için yerel olarak Visual Studio 64 bit çalışan işlemi (msvsmon.exe) 32-bit Visual Studio işlemi içinde gerçekleştirilemez alt düzey işlemleri gerçekleştirmek için kullanır.

 .NET Framework 3.5 veya daha önceki bir sürümünü kullanan 64 bit işlemleri için karışık mod hata ayıklaması desteklenmiyor.

## <a name="debug-a-64-bit-application"></a>Bir 64 bit uygulamanın hatalarını ayıklama
 Bir 64 bit uygulamanın hatalarını ayıklamaya denemek için:

1.  Visual Studio çözümü, örneğin bir C# konsol uygulaması oluşturun.

2.  Yapılandırma Yöneticisi'ni kullanarak 64-bit yapılandırmasını ayarlayın. Daha fazla bilgi için [nasıl yapılır: Projeleri hedef platformlar için yapılandırma](../ide/how-to-configure-projects-to-target-platforms.md).

3.  Bu aşamada, uzaktan hata ayıklayıcı (msvsmon.exe) 64 bit sürümü başlatır. 64-bit yapılandırmayla çözümünün açık olduğu sürece çalıştırır.

4.  Hata ayıklama başlatılamıyor. Aynı deneyimi, 32-bit yapılandırmasına sahip olmalıdır. Hatalarla karşılaşırsanız, aşağıdaki sorun giderme bölümüne bakın.

## <a name="troubleshooting-64-bit-debugging"></a>64-bit hata ayıklama sorunlarını giderme
 Bir hata görebilirsiniz: "Bir 64 bit hata ayıklama işlemi beklenenden uzun sürüyor." Bu durumda, Visual Studio msvsmon.exe 64-bit sürümü için bir istek gönderdi ve geri dönmeniz bu isteğin sonucu için uzun sürdü.

 Bu hata iki ana nedeni vardır:

-   Ağ güvenlik yazılımı güvenilir olmadığı ağ yığınını neden bilgisayarınızda yüklü olması ve localhost üzerinde giden paketlerin bıraktı. Tüm ağ güvenlik yazılımı devre dışı bırakmayı deneyin ve bu da çözmediğine bakın. Bu durumda, rapor, yazılım, localhost trafiğiyle engel ağ güvenlik yazılım satıcınıza için.

-   Visual Studio ile bir yanıt vermemesine veya performans sorunu içine çalışıyor. Sorun düzenli olarak ortaya Visual Studio (devenv.exe) ve çalışan işleminden (msvsmon.exe) dökümleri toplayın ve bunları Microsoft'a gönderin. Bir sorun bildirme hakkında daha fazla bilgi için bkz: [Visual Studio ile ilgili bir sorun bildirme](../ide/how-to-report-a-problem-with-visual-studio.md).

## <a name="see-also"></a>Ayrıca Bkz.

- [64 bit Uygulamalar](https://docs.microsoft.com/dotnet/framework/64-bit-apps)
- [Programları 64 Bit için yapılandırma](/cpp/build/configuring-programs-for-64-bit-visual-cpp)
- [Visual Studio IDE 64 Bit Desteği](../ide/visual-studio-ide-64-bit-support.md)
- [Döküm Dosyalarını Kullanma](../debugger/using-dump-files.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)