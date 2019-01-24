---
title: Idiasession::put_loadaddress | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::put_loadAddress method
ms.assetid: b157b245-1ea0-4b80-8962-d8b278dbc742
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1be0bfd6d5a635dcff632e25421922697b3f0de6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794316"
---
# <a name="idiasessionputloadaddress"></a>IDiaSession::put_loadAddress
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yükleme adresine karşılık gelen yürütülebilir dosyası için sembolleri bu sembol deposu içerisinde ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT put_loadAddress (   
   ULONGLONG NewVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `NewVal`  
 [in] Yürütülebilir dosya için adres yükleyin.  
  
## <a name="remarks"></a>Açıklamalar  
 Sembol sanal adres (VA) özellikleri, bu yöntem değeri kullanılarak hesaplanır. Bu özellik sıfır olmayan ayarlanmadığı sürece sanal adresleri hesaplanmaz.  
  
> [!NOTE]
>  Aldığınızda, bu yöntemi çağırmanız gerekir [Idiasession](../../debugger/debug-interface-access/idiasession.md) başlamadan önce sanal özellikler üzerinde sembolleri kullanmanız gerekiyorsa nesneyi kullanmayı ve nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
