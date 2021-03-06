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
ms.openlocfilehash: c2c9a8b15b5095ac346ba047d6668aada7647a31
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412431"
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
> Çalışma zamanı hata, dil altyapısı yığın çerçevelerini numaralandırma veya nevyhodnocovat gibi görevleri gerçekleştirmek için iş parçacığı tarafından çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [Iactivescripterrordebug arabirimi](../../winscript/reference/iactivescripterrordebug-interface.md)   
 [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md)   
 [BREAKRESUMEACTION numaralandırması](../../winscript/reference/breakresumeaction-enumeration.md)   
 [ERRORRESUMEACTION Sabit Listesi](../../winscript/reference/errorresumeaction-enumeration.md)