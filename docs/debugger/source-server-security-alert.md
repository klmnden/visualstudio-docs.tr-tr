---
title: Kaynak sunucu güvenlik uyarısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.sourceserver.enablewarning
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: 8451c281-6914-469c-b80c-6271cc3f3d17
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: af216023b1a157136f86f0ca8527a8b433b0a34b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719151"
---
# <a name="source-server-security-alert"></a>Kaynak Sunucu Güvenlik Uyarısı
Kaynak Sunucusu'nu kullanırken, yalnızca bilinen ve güvenilen bir konumdan gelen simge dosyalarını kullanın.

 Kaynak sunucu desteğini etkinleştirdiğinizde, bu uyarı görüntülenir. Kaynak sunucu komutları hata ayıklama simge dosyalarına katıştırılmış (**\*.pdb** dosyaları). PDB dosyalarınızın nereden geldiğini bildiğinizden emin olun.

> [!IMPORTANT]
>  Kaynak Sunucusu'nu kullanırken, aşağıdaki olası güvenlik tehditlerini hesaba atılmalıdır: Rastgele komutlar uygulamanın PDB dosyasına eklenebilir, bu nedenle, sadece srcsrv.ini dosyasında yürütmek istediğiniz istediklerinizi koyduğunuzdan emin olun. srcsvr.ini dosyasında olmayan bir komutu yürütme girişimi, bir onay iletişim kutusunun görüntülenmesine neden olur. Daha fazla bilgi için [güvenlik uyarısı: Hata ayıklayıcı güvenilmeyen komut yürütme gerekir](../debugger/security-warning-debugger-must-execute-untrusted-command.md). Komut parametrelerinde bir doğrulama yapılmadı, bu nedenle güvenilir komutlara dikkat edin. Örneğin, cmd.exe'ye güvendiyseniz, kötü niyetli bir kullanıcı, komutu tehlikeli duruma getirecek parametreler belirtebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)
- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Kaynak sunucu](/windows/desktop/Debug/source-server-and-source-indexing)
