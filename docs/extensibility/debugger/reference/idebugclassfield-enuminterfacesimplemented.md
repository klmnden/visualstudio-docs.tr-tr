---
title: IDebugClassField::EnumInterfacesImplemented | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::EnumInterfacesImplemented
helpviewer_keywords:
- IDebugClassField::EnumInterfacesImplemented method
ms.assetid: e5523e45-d350-491e-a92c-fe0ca97d2052
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bffae40f1e5212132c89b6b71b7fc83cca6ebb42
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56702141"
---
# <a name="idebugclassfieldenuminterfacesimplemented"></a>IDebugClassField::EnumInterfacesImplemented
Bu sınıf tarafından uygulanan arabirimler için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumInterfacesImplemented( 
   IEnumDebugFields** ppEnum
);
```

```csharp
int EnumInterfacesImplemented(
   out IEnumDebugFields ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `ppEnum`

 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) uygulanan arabirimlerin listesini temsil eden nesne. Arabirimlerine yoksa null değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya bu sınıfa uygulanan arabirim varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Her öğenin sabit bir [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) bir arabirim tanımlayan nesne. Yönetilmeyen Not [!INCLUDE[vcprvc](../../../code-quality/includes/vcprvc_md.md)] kod bu yöntem her zaman için yönetilmeyen bir null değer döndürecek şekilde ayrık bir varlık olarak arabirimleri kullanmayan [!INCLUDE[vcprvc](../../../code-quality/includes/vcprvc_md.md)] kod.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)