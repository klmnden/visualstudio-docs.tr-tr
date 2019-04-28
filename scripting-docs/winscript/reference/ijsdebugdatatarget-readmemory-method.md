---
title: Ijsdebugdatatarget::readmemory yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.ReadMemory
apilocation:
- jscript9diag.dll
ms.assetid: 664e0f7d-2007-45f4-b993-36fe8b1944e5
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 705fff3bf2d4be78897c18c5a4c61bd74a8c2230
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62582369"
---
# <a name="ijsdebugdatatargetreadmemory-method"></a>IJsDebugDataTarget::ReadMemory Yöntemi
Hedef işlemin belleğini okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ReadMemory(  
   UINT64 address,  
   JsDebugReadMemoryFlags flags,  
   BYTE *pBuffer,  
   DWORD size,  
   DWORD *pBytesRead  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `address`  
 [in] Hedef işlemin belleğinin okunacağı temel adres.  
  
 `flags`  
 [in] ReadMemory davranışını denetleyen bayraklar.  
  
 `pBuffer`  
 [out] Hedef işlemin adres alanından içerikleri alan arabellek. Hata olduğunda, bu arabelleğin içeriği belirtilmez.  
  
 `size`  
 [in] İşlemden okunacak bayt sayısı.  
  
 `pBytesRead`  
 [out] Hedef işlemden okunan bayt sayısını gösterir. Başarı JsDebugAllowPartialRead açık ise, bu değer her zaman tam olarak girdi boyutuna eşit olur. JsDebugAllowPartialRead belirtilirse, başarı durumunda bu değer sıfırdan büyük olacaktır.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Başarılıysa S_OK döndürür başarı ve hata kodları herhangi bir hata için kullanılır. Adres geçerli değilse, e_jsdebug_ınvalıd_memory_address döndürür. Daha fazla bilgi için bkz. JsDebugAllowPartialRead.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)