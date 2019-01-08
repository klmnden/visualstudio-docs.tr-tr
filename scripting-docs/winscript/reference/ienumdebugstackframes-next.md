---
title: IEnumDebugStackFrames::Next | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugStackFrames.Next
apilocation:
- jscript.dll
helpviewer_keywords:
- IEnumDebugStackFrames::Next
ms.assetid: ade3f5b0-8ff3-48a0-9433-270789e6d53e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1366a33a9b6ea4bcfe9e0bb61cf8c61500853e7c
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54092034"
---
# <a name="ienumdebugstackframesnext"></a>IEnumDebugStackFrames::Next
Belirtilen bir numaralandırma sıralı segmentleri sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Next(  
   ULONG                       celt,  
   DebugStackFrameDescriptor*  prgdsfd,  
   ULONG*                      pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Alınacak Segment sayısı.  
  
 `prgdsfd`  
 [out] Bir dizi döndürür `DebugStackFrameDescriptor` alınmasını segmentleri temsil eden arabirim.  
  
 `pceltFetched`  
 [out] Numaralandırıcı tarafından alınan parçaları gerçek sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, belirtilen sayıda sabit listesi sırası segmentler alır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ienumdebugstackframes arabirimi](../../winscript/reference/ienumdebugstackframes-interface.md)   
 [DebugStackFrameDescriptor Yapısı](../../winscript/reference/debugstackframedescriptor-structure.md)