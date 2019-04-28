---
title: Kaynak sunucu güvenlik uyarısı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.sourceserver.enablewarning
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 8451c281-6914-469c-b80c-6271cc3f3d17
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cc7c68fe767d2add0842e30f66c51a3dcc84905f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63447294"
---
# <a name="source-server-security-alert"></a>Kaynak Sunucu Güvenlik Uyarısı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kaynak Sunucusu'nu kullanırken, yalnızca bilinen ve güvenilen bir konumdan gelen simge dosyalarını kullanın.  
  
 Kaynak sunucu desteğini etkinleştirdiğinizde, bu uyarı görüntülenir. Kaynak sunucu komutları hata ayıklama simge dosyalarına (PDB dosyaları) gömülüdür. PDB dosyalarınızın nereden geldiğini bildiğinizden emin olun.  
  
> [!IMPORTANT]
> Kaynak Sunucusu'nu kullanırken, aşağıdaki olası güvenlik tehditlerini hesaba atılmalıdır: Rastgele komutlar uygulamanın PDB dosyasına eklenebilir, bu nedenle, sadece srcsrv.ini dosyasında yürütmek istediğiniz istediklerinizi koyduğunuzdan emin olun. srcsvr.ini dosyasında olmayan bir komutu yürütme girişimi, bir onay iletişim kutusunun görüntülenmesine neden olur. Daha fazla bilgi için [güvenlik uyarısı: Hata ayıklayıcı güvenilmeyen komut yürütme gerekir](../debugger/security-warning-debugger-must-execute-untrusted-command.md). Komut parametrelerinde doğrulama yapılmadı, bu nedenle güvenilir komutlara dikkat edin. Örneğin, cmd.exe'ye güvendiyseniz, kötü niyetli bir kullanıcı, komutu tehlikeli duruma getirecek parametreler belirtebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol (.pdb) belirtin ve kaynak dosyaları](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)   
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Kaynak sunucu](http://msdn.microsoft.com/library/windows/desktop/ms680641.aspx)
