---
title: IDebugClassField::GetDefaultIndexer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::GetDefaultIndexer
helpviewer_keywords:
- IDebugClassField::GetDefaultIndexer method
ms.assetid: 47ce4f45-3816-4b40-909c-5032d0692d75
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: eaaddbe6bb223e8e2987f8310f1d8e08d5602a01
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66206825"
---
# <a name="idebugclassfieldgetdefaultindexer"></a>IDebugClassField::GetDefaultIndexer
Varsayılan oluşturucunun adını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDefaultIndexer( 
   BSTR* pbstrIndexer
);
```

```csharp
int GetDefaultIndexer(
   out string pbstrIndexer
);
```

## <a name="parameters"></a>Parametreler
`pbstrIndexer` [out] Varsayılan oluşturucunun adını içeren bir dize döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya varsayılan dizin oluşturucu yok ise S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir sınıfın varsayılan oluşturucusu olarak işaretlenmiş özelliktir `Default` özelliği için dizi erişir. Bu özel [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)]. İşte bir örnek olarak bildirilen bir varsayılan dizin oluşturucu [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)] ve nasıl kullanılır.

```vb
Imports System.Collections;

Public Class Class1
    Private myList as Hashtable

    Default Public Property Item(ByVal Index As Integer) As Integer
        Get
            Return CType(List(Index), Integer)
        End Get
        Set(ByVal Value As Integer)
            List(Index) = Value
        End Set
    End Property
End Class

Function GetItem(Index as Integer) as Integer
    Dim classList as Class1 = new Class1
    Dim value as Integer

    ' Access array through default indexer
    value = classList(2)

    ' Access array through explicit property
    value = classList.Item(2)

    Return value
End Function
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)