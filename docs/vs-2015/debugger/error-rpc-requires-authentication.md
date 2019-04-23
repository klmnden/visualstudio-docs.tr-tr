---
title: 'Hata: RPC kimlik doğrulaması gerektiriyor | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.rpc_requires_authentication
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 88362b3b-8fbe-431f-96a4-80e2d822bbc7
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: dbf0c2d13668dbf380f326ee3a49e0389815a8fd
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60102737"
---
# <a name="error-rpc-requires-authentication"></a>Hata: RPC kimlik doğrulaması gerektiriyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hata ayıklayıcı uzak bilgisayara bağlanamıyor. Yerel bilgisayarda uzaktan hata ayıklamayı engelleyen bir RPC ilkesi etkin.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. Çalıştırma `\` *windir*`\system32\regedt32.exe`  
  
2. Bulun ve Sil `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows NT\RPC\RestrictRemoteClients`.  
  
3. Kayıt defteri değişikliği etkili şekilde bilgisayarınızı yeniden başlatın.  
  
4. Sorun devam ederse, ilgili etki alanı yöneticinizle iletişime **bilgisayar yapılandırması -> Yönetici Şablonları - > Sistem -> uzak yordam çağrısı, kimliği doğrulanmamış RPC istemciler için kısıtlamaları ->** grubu ilke ayarı.
