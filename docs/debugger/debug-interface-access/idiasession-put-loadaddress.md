---
title: Idiasession::put_loadaddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::put_loadAddress method
ms.assetid: b157b245-1ea0-4b80-8962-d8b278dbc742
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: de23c511f238578de2492992556b557c051841db
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53956994"
---
# <a name="idiasessionputloadaddress"></a>IDiaSession::put_loadAddress
Yükleme adresine karşılık gelen yürütülebilir dosyası için sembolleri bu sembol deposu içerisinde ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
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