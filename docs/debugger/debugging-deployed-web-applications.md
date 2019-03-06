---
title: Dağıtılan bir ASP.NET uygulamalarında hata ayıklama | Microsoft Docs
ms.date: 06/30/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- ASP.NET Web applications
- Web services, debugging
- XML, debugging Web services
- debugging Web services
- ASP.NET, debugging Web applications
- XML Web services, debugging
ms.assetid: b938a91b-be96-416f-83bc-4177e7f3929a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 57594775afe5d6708cd5d11b141f8cffc1b42e6c
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57525394"
---
# <a name="debugging-deployed-aspnet-applications"></a>Dağıtılan bir ASP.NET uygulamalarında hata ayıklama
Kullanılacak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] dağıtılan bir uygulamada hata ayıklamak için iliştirmeniz gerekir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlem ve hata ayıklayıcı semboller için uygulama erişimi olduğundan emin olun. Ayrıca, uygulama için kaynak dosyalarını bulun ve gerekir. Daha fazla bilgi için [belirtin sembol (.pdb) ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md), [nasıl yapılır: ASP.NET işleminin adını bulma](../debugger/how-to-find-the-name-of-the-aspnet-process.md), ve [sistem gereksinimleri](../debugger/aspnet-debugging-system-requirements.md).

> [!WARNING]
> İçin eklerseniz [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi hata ayıklama ve bir kesme noktası İsabeti için tüm yönetilen kod içinde çalışan işlemi durur. Çalışan işlemi tüm yönetilen kodda durdurma iş kesinti tüm kullanıcılar için sunucu üzerinde neden olabilir. Bir üretim sunucusunda hata ayıklama önce Üretim iş olası etkisini göz önünde bulundurun.

Ekleme işlemi [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] çalışan işlemi olan tüm diğer uzak işlemine iliştirme ile aynı. Doğru Proje Aç yoksa, bağlı olduğunuz, uygulama kesildiğinde bir iletişim kutusu görüntülenir. Bu iletişim kutusunu uygulama için kaynak dosyalarının konumunu ister. İletişim kutusunda belirttiğiniz dosya adı, Web sunucusunda hata ayıklama sembolleri içinde belirtilen dosya adı eşleşmelidir. Daha fazla bilgi için [çalışan işlemlere ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md). IIS üzerinde uzaktan hata ayıklamayı kurma için bkz: [uzak bir IIS bilgisayarda uzaktan hata ayıklama ASP.NET](../debugger/remote-debugging-aspnet-on-a-remote-iis-computer.md).

> [!NOTE]
>  Birçok [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Web uygulamaları, iş mantığı ya da diğer kullanışlı bir kod içeren dll başvurusu. Uygulamanızı dağıtırken, böyle bir başvuruyu DLL kullanarak yerel bilgisayarınızdan Web uygulamasının sanal dizin \bin klasörüne kopyalar. Hata ayıklama, Web uygulamanıza dll, kopyalama ve kopya değil, yerel bilgisayarınızda başvuran unutmayın.

## <a name="see-also"></a>Ayrıca Bkz.
- [ASP.NET uygulamalarında hata ayıklama](../debugger/how-to-enable-debugging-for-aspnet-applications.md)
- [Nasıl yapılır: ASP.NET Uygulamaları için Hata Ayıklamayı Etkinleştirme](../debugger/how-to-enable-debugging-for-aspnet-applications.md)
- [Nasıl yapılır: ASP.NET İşleminin Adını Bulma](../debugger/how-to-find-the-name-of-the-aspnet-process.md)
- [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)