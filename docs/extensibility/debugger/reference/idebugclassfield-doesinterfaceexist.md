---
title: IDebugClassField::DoesInterfaceExist | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::DoesInterfaceExist
helpviewer_keywords:
- IDebugClassField::DoesInterfaceExist method
ms.assetid: cc0c8642-1a76-4fda-a309-7018a34883c9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7884bff62321ed07c3a11a6db65855b1edea0adc
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56688413"
---
# <a name="idebugclassfielddoesinterfaceexist"></a>IDebugClassField::DoesInterfaceExist
Belirli bir arabirim sınıfta tanımlı olup olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT DoesInterfaceExist( 
   LPCOLESTR pszInterfaceName
);
```

```csharp
int DoesInterfaceExist(
   [In] string pszInterfaceName
);
```

#### <a name="parameters"></a>Parametreler
 `pszInterfaceName`

 [in] Arabirim adı, aranacak içeren bir dize.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür, S_FALSE döndürür arabirimi yoksa, Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, geçerli tüm arabirimleri numaralandırmasını alır ve eşleşen bir arabirim için liste arar.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)