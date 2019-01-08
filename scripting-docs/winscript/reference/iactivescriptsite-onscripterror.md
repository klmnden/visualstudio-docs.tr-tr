---
title: IActiveScriptSite::OnScriptError | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.OnScriptError
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_OnScriptError
ms.assetid: 5c9c85cc-21ad-4232-be83-a24cc7570108
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d2c9cb95615ad0b978cc7fd9943b687e5a7f3cac
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54088419"
---
# <a name="iactivescriptsiteonscripterror"></a>IActiveScriptSite::OnScriptError
Ana bilgisayara altyapısı betik çalıştırılırken bir yürütme hatası oluştu bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnScriptError(  
    IActiveScriptError *pase  // address of error interface  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pase`  
 [in] Hata nesnenin adresini [Iactivescripterror](../../winscript/reference/iactivescripterror.md) arabirimi. Bir konak, yürütme hatası hakkında bilgi edinmek için bu arabirimi kullanabilirsiniz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` hata doğru işlenmiş ya da OLE tanımlı hata kodu Aksi takdirde.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)