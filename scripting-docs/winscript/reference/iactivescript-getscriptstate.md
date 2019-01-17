---
title: IActiveScript::GetScriptState | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptState
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptState
ms.assetid: 59837f7c-755d-45c4-8194-bd57638fe2e1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a64067679e1c56831002494c579ffdeba84a1abe
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346637"
---
# <a name="iactivescriptgetscriptstate"></a>IActiveScript::GetScriptState
Komut dosyası altyapısının geçerli durumunu alır. Temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan, bu yöntem temel olmayan iş parçacığından çağrılabilir [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) arabirimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptState(  
    SCRIPTSTATE *pss  // address of structure for state information  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pss`  
 [out] Tanımlanan bir değeri alan değişkenin adresini [SCRIPTSTATE numaralandırması](../../winscript/reference/scriptstate-enumeration.md) sabit listesi. Değeri, çağıran iş parçacığı ile ilişkili komut dosyası altyapısının geçerli durumunu gösterir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_POINTER` durumunda geçersiz işaretçi belirtildi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)