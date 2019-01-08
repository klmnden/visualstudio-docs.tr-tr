---
title: Ijsdebugdatatarget::gettlsvalue metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.GetTlsValue
apilocation:
- jscript9diag.dll
ms.assetid: db575be9-7b24-45c5-9008-e4f2f76d6757
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8f81e9ea6cca9bf54753a496e07903d23bb913fc
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095335"
---
# <a name="ijsdebugdatatargetgettlsvalue-method"></a>IJsDebugDataTarget::GetTlsValue Metodu
Hatası ayıklanmakta olan iş parçacığı, belirli TLS dizini için iş parçacığı yerel depolama (TLS) yuvasındaki değeri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetTlsValue(  
   DWORD threadId,  
   UINT32 tlsIndex,  
   UINT64 *pValue  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `threadId`  
 [in] Okunacak hedef işlemde çalışan iş parçacığı.  
  
 `tlsIndex`  
 [in] Hedef işlem TlsAlloc işlevini çağırdığında, ayrılmış olan TLS dizini.  
  
 `pValue`  
 [out] İş parçacığının TLS yuvasında depolanan işaretçi boyutlu değer. Hedef iş parçacığı 32-bit ise, bu değerin üst 32-biti sıfır olacaktır.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Bir işlemin her bir iş parçacığı her TLS dizini için kendi yuvasına sahiptir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)