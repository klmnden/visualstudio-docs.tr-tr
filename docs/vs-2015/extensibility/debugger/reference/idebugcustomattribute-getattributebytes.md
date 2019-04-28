---
title: IDebugCustomAttribute::GetAttributeBytes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCustomAttribute::GetAttributeBytes
helpviewer_keywords:
- IDebugCustomAttribute::GetAttributeBytes
ms.assetid: cf34583b-6530-4dcc-89f8-eb27e4e8d594
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b7813e8e3131b04dc7174b5b666950dd68a6060a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62569079"
---
# <a name="idebugcustomattributegetattributebytes"></a>IDebugCustomAttribute::GetAttributeBytes
Bir blobu bayt olarak öznitelik bilgileri alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAttributeBytes( 
   BYTE*  ppBlob,
   DWORD* pdwLen
);
```

```csharp
int GetAttributeBytes(
   ref byte[] ppBlob,
   ref uint   pdwLen
);
```

#### <a name="parameters"></a>Parametreler
 `ppBlob`

 [out içinde] Öznitelik bayt ile doldurulmuş bir dizi.

 `pdwLen`

 [out içinde] Bayt olarak döndürülecek en fazla sayısını belirtir `ppBlob` dizisi ve diziye gerçekte yazılan bayt sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Ayarlama `ppBlob` kullanılabilir bayt sayısını döndürmek için bir null değer parametresi öznitelikleri. Ardından bir dizi ayırmak ve geçirmek için bu dizide `ppBlob` parametresi.

 Öznitelik bayt özel özniteliğinin ham verileri temsil eder.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)