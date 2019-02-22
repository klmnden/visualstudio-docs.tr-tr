---
title: IDebugProcess2::GetAttachedSessionName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::GetAttachedSessionName
helpviewer_keywords:
- IDebugProcess2::GetAttachedSessionName
ms.assetid: 7e5e116f-2c0c-4bc8-ad3f-e9fd2318a7e4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: aa932817c796249803558ad1eb877f620198b3e4
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703556"
---
# <a name="idebugprocess2getattachedsessionname"></a>IDebugProcess2::GetAttachedSessionName
Bu işlem hata ayıklama oturumu adını alır. Bir IDE bir kullanıcı belirli bir makinenin belirli bir işlemde hata ayıklama için bu bilgileri görüntüleyebilirsiniz.

> [!NOTE]
>  Bu metot kullanımdan kaldırılmıştır ve uygulaması her zaman döndürmelidir `E_NOTIMPL`.

## <a name="syntax"></a>Sözdizimi

```
HRESULT GetAttachedSessionName(
   BSTR* pbstrSessionName
);
```

#### <a name="parameters"></a>Parametreler
 `pbstrSessionName`

## <a name="return-value"></a>Dönüş Değeri
 Bu yöntem her zaman döndürmelidir `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)