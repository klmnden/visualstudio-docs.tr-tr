---
title: Ijsdebugdatatarget::writememory yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.WriteMemory
apilocation:
- jscript9diag.dll
ms.assetid: 0d3c04c3-9ef8-4842-a145-3d29bca75062
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 622de16cc5f755c5d69059a0e0f28d881121861c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153818"
---
# <a name="ijsdebugdatatargetwritememory-method"></a>IJsDebugDataTarget::WriteMemory Yöntemi
Hedef işlemin belleğini okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT WriteMemory(  
   UINT64 address,  
   const BYTE *pMemory,  
   DWORD size  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `address`  
 [in] Hedef işlemin belleğinin yazılacağı temel adres.  
  
 `pMemory`  
 [in] Belirli bir işlemin adres alanında yazılacak veriler.  
  
 `size`  
 [in] İşleme yazdırılacak bayt sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Veri aktarımı gerçekleşmeden önce sistem temel adreste ve belirtilen boyut, bellek, tüm verilerin yazma erişimi için erişilebilir olduğundan ve erişilebilir değilse işlev e_jsdebug_ınvalıd_memory_address hatası verir. doğrular.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)