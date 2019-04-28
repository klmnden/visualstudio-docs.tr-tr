---
title: IActiveScriptSiteDebug::OnScriptErrorDebug | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteDebug.OnScriptErrorDebug
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteDebug::OnScriptErrorDebug
ms.assetid: 87f201da-36eb-49a2-b000-e1e1e8c4cdb7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 50e8c7baa42d6f2f36dc71b768797dfe2a464bf3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992422"
---
# <a name="iactivescriptsitedebugonscripterrordebug"></a>IActiveScriptSiteDebug::OnScriptErrorDebug
Çalışma zamanı hatalarının nasıl işleneceğini belirlemek bir akıllı ana bilgisayar sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnScriptErrorDebug(  
   IActiveScriptErrorDebug*  pErrorDebug,  
   BOOL*                     pfEnterDebugger,  
   BOOL*                     pfCallOnScriptErrorWhenContinuing  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pErrorDebug`  
 [in] Çalışma zamanı hata oluştu  
  
 `pfEnterDebugger`  
 [out] JIT hata ayıklama yapmak için hata ayıklayıcı hata geçirmek etkinleştirilip etkinleştirilmeyeceğini belirten bayrak.  
  
 `pfCallOnScriptErrorWhenContinuing`  
 [out] Çağrılıp çağrılmayacağını belirten bayrak `IActiveScriptSite::OnScriptError` kullanıcı ne zaman karar hata ayıklama olmadan devam etmek.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler içerir, ancak aşağıdaki tabloda değeri sınırlı değildir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir akıllı ana bilgisayar, çalışma zamanı hatalarının nasıl işleneceğini belirlemek için bu yöntemi kullanabilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteDebug Arabirimi](../../winscript/reference/iactivescriptsitedebug-interface.md)