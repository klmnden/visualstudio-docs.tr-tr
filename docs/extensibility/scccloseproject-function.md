---
title: SccCloseProject işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccCloseProject
helpviewer_keywords:
- SccCloseProject function
ms.assetid: 259c2069-d349-4814-810f-1c3151b7fb84
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0420aa4d7148e6409dd6edab903ffbc3e7644f35
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683856"
---
# <a name="scccloseproject-function"></a>SccCloseProject işlevi
Bu işlev, belirli bir oturum sonunu işaretlemek için bir proje, kapatır.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccCloseProject (
   LPVOID pvContext
);
```

### <a name="parameters"></a>Parametreler
 Kaynak Denetimi Eklentisi context yapısını pvContext.

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Proje başarıyla kapatıldı.|
|SCC_E_PROJNOTOPEN|Proje şu anda açıktır.|
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 [SccOpenProject](../extensibility/sccopenproject-function.md) her zaman önce bu işlev çağrılır. Bu işlev çağrısı öğelerine yönelik çağrıdan sonra takip `SccOpenProject` işlevi veya [SccUninitialize](../extensibility/sccuninitialize-function.md), sona erdiği kaynak denetim sistemi bağlantısı tamamen.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [SccOpenProject](../extensibility/sccopenproject-function.md)
- [SccInitialize](../extensibility/sccinitialize-function.md)