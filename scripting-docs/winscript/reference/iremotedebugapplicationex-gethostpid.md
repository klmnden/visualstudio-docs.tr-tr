---
title: IRemoteDebugApplicationEx:GetHostPid | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationEx:GetHostPid
apilocation:
- scrobj.dll
helpviewer_keywords:
- IRemoteDebugApplicationEx:GetHostPid
ms.assetid: 4cf9f46c-29cf-4201-87f0-5b1ddbed2f2b
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d660cce006e7f84f1b1c01f1ec0a406b5c4b9df3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62934582"
---
# <a name="iremotedebugapplicationexgethostpid"></a>IRemoteDebugApplicationEx:GetHostPid

Konak uygulamanın işlem Kimliğini döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetHostPid(
   DWORD*  dwHostPid
);
```

### <a name="parameters"></a>Parametreler

`dwHostPid`

[out] Ana bilgisayar işlemi tanımlayıcısı.

## <a name="return-value"></a>Dönüş Değeri

Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:

|Değer|Açıklama|
|-----------|-----------------|
|`S_OK`|Yöntem başarılı oldu.|

## <a name="remarks"></a>Açıklamalar

IDE tarafından kullanılır.

## <a name="see-also"></a>Ayrıca bkz.

- [IRemoteDebugApplicationEx Arabirimi](iremotedebugapplicationex-interface.md)