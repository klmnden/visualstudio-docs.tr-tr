---
title: IRemoteDebugApplicationEx:ForceStepMode | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 3cb5c94c55709f5ecdbd6bae63ee3366f3dfeb2f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790860"
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