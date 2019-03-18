---
title: IDebugApplication::HandleRuntimeError | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.HandleRuntimeError
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::HandleRuntimeError
ms.assetid: f8f3bbaf-09e5-4d01-8a35-f380bc7ff8ed
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0a457ba0dcc6fb7f8a95a982b6dabd93f9d0207e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58150107"
---
# <a name="idebugapplicationhandleruntimeerror"></a>IDebugApplication::HandleRuntimeError
Geçerli iş parçacığını engellemek neden olur ve hata ayıklayıcıya IDE hatanın bir bildirim gönderir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT HandleRuntimeError(  
   IActiveScriptErrorDebug*  pErrorDebug,  
   IActiveScriptSite*        pScriptSite,  
   BREAKRESUMEACTION*        pbra,  
   ERRORRESUMEACTION*        perra,  
   BOOL*                     pfCallOnScriptError  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pErrorDebug`  
 [in] Gerçekleşen hata.  
  
 `pScriptSite`  
 [in] İş parçacığının betik sitesi.  
  
 `pbra`  
 [out] Hata ayıklayıcı uygulama devam ettiğinde gerçekleştirilecek eylem.  
  
 `perra`  
 [out] Bir hata varsa hata ayıklayıcı uygulama devam ettiğinde gerçekleştirilecek eylem.  
  
 `pfCallOnScriptError`  
 [out] Olan bayrağı `TRUE` altyapısı çağırırsanız `IActiveScriptSite::OnScriptError` yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir dil altyapısı, bir çalışma zamanı hatası neden olan bir iş parçacığının bağlamında bu yöntemi çağırır. Bu yöntem geçerli iş parçacığını engelleme neden olur ve IDE hata ayıklayıcı için gönderilecek bir hata bildirimi gönderir. IDE hata ayıklayıcı uygulama devam ettiğinde, bu yöntem gerçekleştirilecek eylem döndürür.  
  
> [!NOTE]
>  Çalışma zamanı hata, dil altyapısı yığın çerçevelerini numaralandırma veya nevyhodnocovat gibi görevleri gerçekleştirmek için iş parçacığı tarafından çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [Iactivescripterrordebug arabirimi](../../winscript/reference/iactivescripterrordebug-interface.md)   
 [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md)   
 [BREAKRESUMEACTION numaralandırması](../../winscript/reference/breakresumeaction-enumeration.md)   
 [ERRORRESUMEACTION Sabit Listesi](../../winscript/reference/errorresumeaction-enumeration.md)