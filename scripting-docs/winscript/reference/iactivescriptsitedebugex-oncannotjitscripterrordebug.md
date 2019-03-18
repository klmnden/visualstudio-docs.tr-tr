---
title: IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSiteDebugEx.OnCanNotJITScriptErrorDebug
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug
ms.assetid: 83f81476-bf12-47f2-897d-1d37d21137d4
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4c643478da37b5a66c22b201ef8f8248df02e4ec
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58154484"
---
# <a name="iactivescriptsitedebugexoncannotjitscripterrordebug"></a>IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug
Konak işlemde hata ayıklamak, Yöneticisi bir komut dosyası çalışma zamanı hatası hakkında tam zamanında betik hata ayıklayıcısı bulamazsa bildirir.  
  
 Bir hata ayıklayıcı, ana bilgisayar uygulamak için işleyeceğini [IActiveScriptSiteDebug::OnScriptErrorDebug](../../winscript/reference/iactivescriptsitedebug-onscripterrordebug.md). Bir kullanıcı eylemine bağlı olarak, konak ya da debugger iliştirebilmek için dönün ve OnScriptErrorDebug hata ayıklayıcıda başlangıç dönüş `pfEnterDebugger` parametresi. Ayrıca, hata ayıklama işlemi Yöneticisi tarafından yorumlanan dış hiçbir hata ayıklayıcıları olsa bile, çalışma zamanı hatası hakkında bildirim almak için bu arabirimi uygulamalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnCanNotJITScriptErrorDebug(  
   IActiveScriptErrorDebug*  pErrorDebug  
   BOOL *pfCallOnScriptErrorWhenContinuing  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pErrorDebug`  
 [in] Çalışma zamanı hata oluştu.  
  
 `pfCallOnScriptErrorWhenContinuingt`  
 [out] Çağrılıp çağrılmayacağını [IActiveScriptSiteDebug::OnScriptErrorDebug](../../winscript/reference/iactivescriptsitedebug-onscripterrordebug.md) hata ayıklama olmadan devam etmek kullanıcı karar verirse.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Ayrıca, bir bildirim almak için bu arabirimi uygulamalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSiteDebugEx Arabirimi](../../winscript/reference/iactivescriptsitedebugex-interface.md)