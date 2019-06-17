---
title: Uzaktan hata ayıklama ve sorun giderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugger, errors
- debugging errors
- remote debugging, troubleshooting
- troubleshooting remote debugging
- errors [debugger], remote debugging
- remote debugging, errors
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 078551111223f11b38f3192075caa9ddfabaf18c
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043333"
---
# <a name="remote-debugging-errors-and-troubleshooting"></a>Uzaktan Hata Ayıklama Hataları ve Sorun Giderme

Uzaktan hata ayıklama çalışılırken şu hatalar arasında gelebilir.

- [Hata: Otomatik Olarak Sunucunun İçine Adımlanamıyor](../debugger/error-unable-to-automatically-step-into-the-server.md)

- [Hata: Microsoft Visual Studio Uzaktan Hata Ayıklama İzleyicisi (MSVSMON.EXE) uzak bilgisayar üzerinde çalışıyor görünmüyor.](/visualstudio/debugger/error-remote-debugging-monitor-msvsmon-exe-does-not-appear-to-be-running)

- [Microsoft Visual Studio Uzaktan Hata Ayıklama İzleyicisi'ne Bağlanılamıyor](../debugger/unable-to-connect-to-the-microsoft-visual-studio-remote-debugging-monitor.md)

- [Hata: Uzak makine, Uzaktan Bağlantılar iletişim kutusunda görünmüyor](../debugger/error-remote-machine-does-not-appear-in-a-remote-connections-dialog.md)

## <a name="run-the-remote-debugger-as-an-administrator"></a>Uzaktan hata ayıklayıcı yönetici olarak çalıştırın

Uzaktan hata ayıklayıcı yönetici olarak çalıştırmazsanız sorunları ortaya çıkabilir. Örneğin, aşağıdaki hatayı görebilirsiniz: "Visual Studio uzaktan hata ayıklayıcı (MSVSMON. EXE) Bu işlemde hata ayıklamak için yeterli ayrıcalığı yok." Uzaktan hata ayıklayıcı bir uygulama (hizmeti değil) olarak çalıştırıyorsanız, görebileceğiniz [farklı kullanıcı hesabınızla](error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-is-running-as-a-different-user.md) hata.

### <a name="when-running-the-remote-debugger-as-a-service"></a>Uzaktan hata ayıklayıcıyı bir hizmet olarak çalışırken

Uzaktan hata ayıklayıcı s hizmet olarak çalışırken, çeşitli nedenlerle yönetici olarak çalıştırarak öneririz:

- Uzaktan hata ayıklayıcı hizmeti bağlantıları olduğundan yöneticilerinin yalnızca sağlar. **hiçbir** yönetici olarak çalıştırarak sunulan yeni güvenlik riskleri.

- Bu Visual Studio kullanıcı uzaktan hata ayıklayıcı kendisini daha bir işlemde hata ayıklamak için daha fazla haklara sahip olduğunda sonuç vermez hataları önleyebilirsiniz.

- Uzaktan hata ayıklayıcı yapılandırma ve Kurulum basitleştirmek için.

Uzaktan hata ayıklayıcı yönetici olarak çalıştırarak olmadan hata ayıklama mümkün olsa da, bu işi doğru şekilde yapmak için birkaç gereksinim vardır ve bunlar genellikle daha gelişmiş hizmeti yapılandırma adımları gerektirir.

- Uzak makinede kullandığınız hesabın olmalıdır **hizmet olarak oturum açma** ayrıcalık. "Oturum açma hizmet olarak ekleme" altındaki adımları görmek [geri bağlanamıyor](error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md) hata.

- Hesap, hedef işlemde hata ayıklamak için haklarına sahip olmalıdır. Bu hakları almak için aynı hesabı altında uzaktan hata ayıklayıcı hata ayıklama işlemi çalıştırmanız gerekir. (Hizmeti bir yönetici olarak çalıştırmak için daha kolay bir alternatif içindir.) 

- Hesap geri (diğer bir deyişle, kimlik doğrulaması için) bağlayabilirsiniz ağ üzerinden Visual Studio bilgisayarı. Bir etki alanı üzerinde geri uzaktan hata ayıklayıcı yerleşik yerel sistem veya ağ hizmeti hesabı veya bir etki alanı hesabı altında çalışıyorsa bağlanmak kolaydır. Yerleşik hesaplar yükseltilmiş bir güvenlik riski sunabilir güvenlik ayrıcalıklara sahip.

### <a name="when-running-the-remote-debugger-as-an-application-normal-mode"></a>Uzaktan hata ayıklayıcı çalışan bir uygulama olarak (normal mod)

(Örneğin, normal bir uygulama) kendi yükseltilmiş olmayan işlem eklemeye çalışıyorsanız, uzaktan hata ayıklayıcı yönetici olarak çalıştırıyorsanız, önemli değildir.

Uzaktan hata ayıklayıcı, çeşitli senaryolarda yönetici olarak çalıştırmak istediğiniz:

- Başka bir kullanıcı olarak çalışan işlemler için eklemek istediğiniz (ne zaman gibi IIS hata ayıklama), veya

- Başka bir işlem başlatmaya çalışıyorsanız ve başlatmak istediğiniz yönetici işlemidir.

Bunu **değil** işlemler başlatabilir ve başlatmak için istediğiniz işlemi gerektiğini istiyorsanız yönetici olarak çalıştırmak istediğiniz **değil** yönetici olabilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)