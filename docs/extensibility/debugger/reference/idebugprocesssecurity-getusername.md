---
title: IDebugProcessSecurity::GetUserName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProcessSecurity::GetUserName
ms.assetid: c73c60ac-da6e-45ae-8f04-95353a24ca3e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 793a3072160230744ab66a5805cd99c24e20cb7c
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200443"
---
# <a name="idebugprocesssecuritygetusername"></a>IDebugProcessSecurity::GetUserName
Kullanıcı adı bağlantı noktası tedarikçiden alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetUserName(
    BSTR *pbstrUserName
);
```

```csharp
int GetUserName (
    string pbstrUserName
);
```

## <a name="parameters"></a>Parametreler
`pbstrUserName`\
[out] Kullanıcı adını içeren bir dize.

## <a name="return-value"></a>Dönüş Değeri
 Yöntem başarılı olursa, döndürür `S_OK`. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 `GetUserName` görüntülenen kullanıcı adını döndürür **kullanıcı adı** sütununun **iliştirme** iletişim kutusu. Görüntülenecek **iliştirme** iletişim kutusu, tıklayın **iliştirme** üzerinde **Araçları** menüde [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE).

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcessSecurity](../../../extensibility/debugger/reference/idebugprocesssecurity.md)