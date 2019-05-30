---
title: IDebugAlias2::GetAppDomainId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- GetAppDomainId
- IDebugAlias2::GetAppDomainId
ms.assetid: 23581aaa-5a53-4859-b264-eca49fc44bcd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b40d52c5eedf0defb845f1944acd166d48dca1ee
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66338167"
---
# <a name="idebugalias2getappdomainid"></a>IDebugAlias2::GetAppDomainId
Uygulama etki alanı için tanımlayıcıyı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAppDomainId (
   ULONG32* pappDomainId
);
```

```csharp
int GetAppDomainId (
   out uint pappDomainId
);
```

## <a name="parameters"></a>Parametreler
`pappDomainId`\
[out] Uygulama etki alanı tanımlayıcısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Uygulama yeniden başlatıldığında uygulama etki alanı tanımlayıcısı değişiklikleri ve yeni bir uygulama etki alanı oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugAlias2](../../../extensibility/debugger/reference/idebugalias2.md)