---
title: Ijsdebug::openvirtualprocess yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJSDebug.OpenVirtualProcess
apilocation:
- jscript9diag.dll
ms.assetid: 5612bf1b-a4e3-4eaf-ac5e-c2e1f147c395
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 97a055bf1550d74dc6b86d93ffdb9ca406afb43d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62583600"
---
# <a name="ijsdebugopenvirtualprocess-method"></a>IJsDebug::OpenVirtualProcess Yöntemi
Yeni bir sanal işlem nesnesi oluşturmak için kullanılan fabrika yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OpenVirtualProcess(  
   DWORD processId,  
   UINT64 runtimeJsBaseAddress,  
   IJsDebugDataTarget *pDataTarget,  
   IJsDebugProcess **ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `processId`  
 [in] Hata ayıklayıcıyı iliştirmek için işlem kimliği'ni kullanın.  
  
 `runtimeJsBaseAddress`  
 [in] Başlangıçtan JavaScript çalışma zamanı hedef işleme yüklendiği temel adres.  
  
 `pDataTarget`  
 [in] Hata ayıklayıcı, işlemin durumunu sorgulamak için sağlanan arabirim.  
  
 `ppProcess`  
 [out] Yeni hata ayıklama işlemi nesnesi  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Jscript9diag ve Jscript9 eşleşmiyorsa, e_jsdebug_mısmatched_runtıme döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebug Arabirimi](../../winscript/reference/ijsdebug-interface.md)