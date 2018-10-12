---
title: 'Hata: RPC kimlik doğrulaması gerektiriyor. | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.rpc_requires_authentication
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 88362b3b-8fbe-431f-96a4-80e2d822bbc7
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5643e815386541bb9045eb56cacbd68e7e9b998d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49193843"
---
# <a name="error-rpc-requires-authentication"></a>Hata: RPC Kimlik Doğrulaması Gerektiriyor
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hata ayıklayıcı uzak bilgisayara bağlanamıyor. Yerel bilgisayarda uzaktan hata ayıklamayı engelleyen bir RPC ilkesi etkin.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1.  Çalıştırma `\` *windir*`\system32\regedt32.exe`  
  
2.  Bulun ve Sil `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows NT\RPC\RestrictRemoteClients`.  
  
3.  Kayıt defteri değişikliği etkili şekilde bilgisayarınızı yeniden başlatın.  
  
4.  Sorun devam ederse, ilgili etki alanı yöneticinizle iletişime **bilgisayar yapılandırması -> Yönetici Şablonları - > Sistem -> uzak yordam çağrısı, kimliği doğrulanmamış RPC istemciler için kısıtlamaları ->** grubu ilke ayarı.



