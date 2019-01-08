---
title: IActiveScriptSiteInterruptPoll::QueryContinue | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteInterruptPoll.QueryContinue
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteInterruptPoll::QueryContinue
ms.assetid: 41ac3807-f8b4-4a0e-bcc6-556bc89f3904
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9b43211dca57a404d5625cfc2d7ede67a70a0a40
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087990"
---
# <a name="iactivescriptsiteinterruptpollquerycontinue"></a>IActiveScriptSiteInterruptPoll::QueryContinue
Bir betik sonlandırması gerektiğini belirtmek bir konak sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT QueryContinue();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Çağrı başarılı oldu ve konak betiği çalıştırmaya devam etmesine izin verir.|  
|`S_FALSE`|Başarılı çağrı ve betik sonlandırma konak istekleri.|  
  
## <a name="remarks"></a>Açıklamalar  
 Barındırılan betik sürece sonlandırması gerektiğini dönüş değerini `QueryContinue` yöntemi `S_OK`. Dönüş değeri `S_FALSE` betik sonlandırma, konak açıkça istekleri gösterir.  
  
 Çok iş parçacıklı bir konak kullanabilir `IActiveScript::InterruptScriptThread` bir betik sonlandırmak için yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iactivescriptsiteınterruptpoll arabirimi](../../winscript/reference/iactivescriptsiteinterruptpoll-interface.md)   
 [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md)