---
title: IRemoteDebugApplicationEx:ForceStepMode | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationEx:ForceStepMode
apilocation:
- scrobj.dll
helpviewer_keywords:
- IRemoteDebugApplicationEx:ForceStepMode
ms.assetid: 83e69a3e-e4c9-4ddd-b01b-1820e4177a03
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04a2c700d2cac4bcdc845ebf442de29863e87deb
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159497"
---
# <a name="iremotedebugapplicationexforcestepmode"></a>IRemoteDebugApplicationEx:ForceStepMode

Tek adımlı modda hata ayıklayıcıya zorlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT ForceStepMode(
   IRemoteDebugApplicationThread*  pStepThread
);
```

### <a name="parameters"></a>Parametreler

`pStepThread`

[in] İş parçacığı için adım adım işlem hata ayıklama İzleyicisi. Null ise, Adımlama, iş parçacığı PDM temizler.

## <a name="return-value"></a>Dönüş Değeri

Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:

|Değer|Açıklama|
|-----------|-----------------|
|`S_OK`|Yöntem başarılı oldu.|

## <a name="see-also"></a>Ayrıca bkz.

- [IRemoteDebugApplicationEx Arabirimi](iremotedebugapplicationex-interface.md)