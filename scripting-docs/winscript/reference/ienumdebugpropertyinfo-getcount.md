---
title: IEnumDebugPropertyInfo::GetCount | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugPropertyInfo.GetCount
apilocation:
- scrobj.dll
helpviewer_keywords:
- IEnumDebugPropertyInfo::GetCount
ms.assetid: 83a3becd-8533-4880-9c4f-193227ff25a9
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 06ed69926b47d8c40c3914acbd2b0208e55f709a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62963448"
---
# <a name="ienumdebugpropertyinfogetcount"></a>IEnumDebugPropertyInfo::GetCount
Sayısını alır `DebugPropertyInfo` yapıları, numaralandırıcı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetCount (  
   ULONG* pcelt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcelt`  
 [out] Sayısını döndürür `DebugPropertyInfo` yapıları, numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Geçerli bir döndürür `HRESULT`, genellikle `S_OK`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ienumdebugpropertyınfo arabirimi](../../winscript/reference/ienumdebugpropertyinfo-interface.md)   
 [DebugPropertyInfo Yapısı](../../winscript/reference/debugpropertyinfo-structure.md)