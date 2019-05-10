---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 887002086b50198ba192bde3f19390d3267a5c9d
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457335"
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
Belirtilen bir arabirim işlem sınırları alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT UnmarshalDebuggeeInterface(
   REFIID riid,
   void** ppvObject
);
```

```csharp
int UnmarshalDebuggeeInterface(
   ref Guid   riid,
   out IntPtr ppvObject
);
```

## <a name="parameters"></a>Parametreler
 `riid`\

 [in] Elde etmek için GUID arabirimi.

 `ppvObject`\

 [out] İstenen arabirimini uygulayan bir nesne döndürür. [C++] Bu doğrudan istenen arabirim türüne çevirebilirsiniz. [C#] kullanın <xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown%2A> istendiği arayüz almak için yöntemi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, hata ayıklama altyapısı çalışırken kullanılır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] işlem alanına ve hata ayıklanan programa kendi işlem alanında çalışıyor.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)