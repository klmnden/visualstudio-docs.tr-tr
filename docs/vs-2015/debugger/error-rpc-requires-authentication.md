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
ms.openlocfilehash: c3393e5a70a0662d15cc4d643f7a5df106860d26
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777685"
---
# <a name="error-rpc-requires-authentication"></a>Hata: RPC kimlik doğrulaması gerektiriyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hata ayıklayıcı uzak bilgisayara bağlanamıyor. Yerel bilgisayarda uzaktan hata ayıklamayı engelleyen bir RPC ilkesi etkin.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Çalıştırma `\` *windir*`\system32\regedt32.exe`  
  
2.  Bulun ve Sil `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows NT\RPC\RestrictRemoteClients`.  
  
3.  Kayıt defteri değişikliği etkili şekilde bilgisayarınızı yeniden başlatın.  
  
4.  Sorun devam ederse, ilgili etki alanı yöneticinizle iletişime **bilgisayar yapılandırması -> Yönetici Şablonları - > Sistem -> uzak yordam çağrısı, kimliği doğrulanmamış RPC istemciler için kısıtlamaları ->** grubu ilke ayarı.
