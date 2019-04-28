---
title: IDebugFunctionObject2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugFunctionObject2 interface
ms.assetid: 56b2fdff-146d-4138-a34c-59a9c65a3ddd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 972cc9af0453668e4d5393a00bb80f34e2594273
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63388450"
---
# <a name="idebugfunctionobject2"></a>IDebugFunctionObject2
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bir işlevi temsil eder ve geliştirir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IDebugFunctionObject2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendiricisi (EE) bir işlevi temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirimin yöntemlerini erteleme içeriğiyle **IDebugFunctionObject** aşağıdaki yollarla:

- **IDebugEvaluate** yöntemi bayrakları alır.

- **CreateObject** yöntemi bayrakları ve bir zaman aşımını alır.

- **CreateStringObjectWithLength** yöntemi bir uzunluğunu alır.

## <a name="methods"></a>Yöntemler
 Bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject2-createobject.md)|Verilen değerlendirme bayrağı ayarlar ve bir zaman aşımı değeri bir oluşturucu kullanan bir nesne oluşturur.|
|[CreateStringObjectWithLength](../../../extensibility/debugger/reference/idebugfunctionobject2-createstringobjectwithlength.md)|Belirtilen uzunlukta bir dize nesnesi oluşturur.|
|[Evaluate](../../../extensibility/debugger/reference/idebugfunctionobject2-evaluate.md)|İşlevini çağırır ve bir nesne olarak elde edilen değeri döndürür.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll