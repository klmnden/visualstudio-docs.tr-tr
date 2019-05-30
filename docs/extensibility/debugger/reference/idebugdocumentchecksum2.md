---
title: IDebugDocumentChecksum2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentChecksum2 interface
ms.assetid: 6d22fa94-21aa-46cb-b5b5-32a6399ebb20
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0b4bfc51595e6414a3760d4e57ab6f9791259f83
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341295"
---
# <a name="idebugdocumentchecksum2"></a>IDebugDocumentChecksum2
Hata ayıklama belge için bir sağlama toplamı temsil eder ve bileşenleri arasında sağlama toplamı geçirme sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugDocumentChecksum2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirimi kullanıma sunan herhangi bir bileşeni tarafından uygulanabilir [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) arabirimi. Ancak, katıştırılmış bir sembol dosyası (*.pdb) sağlama toplamı IDE geçirilen ve bir kaynağı bulma işleminde kullanılan hata ayıklama motoru tarafından temelde uygulandığı.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentChecksum2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetChecksumAndAlgorithmId](../../../extensibility/debugger/reference/idebugdocumentchecksum2-getchecksumandalgorithmid.md)|Kullanılacak bayt sayısı belirtilen belge sağlama toplamı ve algoritma tanımlayıcısını alır.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll