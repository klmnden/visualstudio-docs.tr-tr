---
title: IDebugProgram3::ExecuteOnThread | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProgram3::ExecuteOnThread
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 798a0caca394a21d6ee12a99efeacb2f27f6969c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66343598"
---
# <a name="idebugprogram3executeonthread"></a>IDebugProgram3::ExecuteOnThread
Hata ayıklayıcı programın yürütür. İş parçacığı üzerinde hangi iş parçacığının kullanıcı program çalıştırılırken görüntüleyen hata ayıklayıcı bilgiler vermemiz döndürülür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT ExecuteOnThread(
   [in] IDebugThread2* pThread)
```

```csharp
int ExecuteOnThread(
   IDebugThread2 pThread
);
```

## <a name="parameters"></a>Parametreler
`pThread`\
[in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir hata ayıklayıcı durduruluyor sonra yürütmeye devam edebilir üç farklı yolu vardır:

- Yürütün: Herhangi bir önceki adımı iptal etmek ve vb. sonraki kesme noktasına kadar çalıştırın.

- Adım: Eski herhangi bir adımı iptal edin ve yeni adım tamamlanana kadar çalıştırın.

- Devam edin: Tekrar çalıştırın ve herhangi bir eski adımı etkin bırakın.

  İş parçacığı geçirilen `ExecuteOnThread` hangi iptal etmek için kullanmak adımda saptarken yararlı olur. Tüm adımları Yürüt çalışan iş parçacığı, bilmiyorsanız, iptal eder. İş parçacığı bilgiyle etkin iş parçacığı üzerinde adımı iptal etmek yeterlidir.

## <a name="see-also"></a>Ayrıca bkz.
- [Execute](../../../extensibility/debugger/reference/idebugprogram2-execute.md)
- [IDebugProgram3](../../../extensibility/debugger/reference/idebugprogram3.md)