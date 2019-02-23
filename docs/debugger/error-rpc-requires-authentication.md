---
title: 'Hata: RPC kimlik doğrulaması gerektiriyor | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.rpc_requires_authentication
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0bf72110e82fc3cd920f571a5630faafbf2aa5ec
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56696538"
---
# <a name="error-rpc-requires-authentication"></a>Hata: RPC kimlik doğrulaması gerektiriyor
Visual Studio hata ayıklayıcı uzak bilgisayara bağlanamıyor. Yerel bilgisayarda uzaktan hata ayıklamayı engelleyen bir RPC ilkesi etkin.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1.  Çalıştırma `\` *windir*`\system32\regedt32.exe`

2.  Bulun ve Sil `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows NT\RPC\RestrictRemoteClients`.

3.  Kayıt defteri değişikliği etkili şekilde bilgisayarınızı yeniden başlatın.

4.  Sorun devam ederse, ilgili etki alanı yöneticinizle iletişime **bilgisayar yapılandırması > Yönetim Şablonları > Sistem > uzak yordam çağrısı > kimliği doğrulanmamış RPC istemciler için kısıtlamaları** Grup İlkesi ayar.