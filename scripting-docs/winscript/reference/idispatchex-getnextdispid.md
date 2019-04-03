---
title: IDispatchEx::GetNextDispID | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispatchEx.GetNextDispID
apilocation:
- scrobj.dll
helpviewer_keywords:
- GetNextDispID method
ms.assetid: 8263d441-85ee-47f4-bdba-fbf2ad07e85f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d964a8744f1f0a28704dd0a1d5e0fd2e67aab1c
ms.sourcegitcommit: 05d104a14ff357d599ff274f97cd59d464ee4a46
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/03/2019
ms.locfileid: "58897679"
---
# <a name="idispatchexgetnextdispid"></a>IDispatchEx::GetNextDispID

Bir nesnenin üyelerine numaralandırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetNextDispID(
   DWORD grfdex,
   DISPID id,
   DISPID *pid
);
```

## <a name="parameters"></a>Parametreler

`grfdex`\
Numaralandırılacak hangi öğeleri kümesi olduğunu belirler. Bu, aşağıdaki değerleri birleşimi olabilir:

|Değer|Açıklama|
|-----------|-------------|
|fdexEnumDefault|İstekler, nesnenin varsayılan öğeleri sıralar. Nesne, herhangi bir öğe kümesini listeleme izin verilmez.|
|fdexEnumAll|İstekleri nesne tüm öğeleri sıralar. Nesne, herhangi bir öğe kümesini listeleme izin verilmez.|

`id`\
Geçerli üye tanımlar. Getnextdispıd numaralandırma sonra bu öğeyi alır. Getdispıd veya önceki bir çağrı Getnextdispıd bu tanımlayıcıyı almak için kullanır. İlk öğenin ilk tanımlayıcısı DISPID_STARTENUM değerini kullanır.

`pid`\
Adresi bir DISPID değişkenin numaralandırmada sonraki öğeye tanımlayıcısını alır.

Bir üye tarafından silinirse `DeleteMemberByName` veya `DeleteMemberByDispID`, `DISPID` için geçerli kalır gerekiyor `GetNextDispID`.

## <a name="return-value"></a>Dönüş Değeri

Aşağıdaki değerlerden birini döndürür:

|||
|-|-|
|`S_OK`|Başarılı.|
|`S_FALSE`|Sabit listesi bitti.|

## <a name="example"></a>Örnek

```cpp
   HRESULT hr;
   BSTR bstrName;
   DISPID dispid;
   IDispatchEx *pdex;

   // Assign to pdex
   hr = pdex->GetNextDispID(fdexEnumAll, DISPID_STARTENUM, &dispid);
   while (hr == NOERROR)
   {
      hr = pdex->GetMemberName(dispid, &bstrName);
      if (!wcscmp(bstrName, OLESTR("Bar")))
      {
         SysFreeString(bstrName);
         return TRUE;
      }
      SysFreeString(bstrName);
      hr = pdex->GetNextDispID(fdexEnumAll, dispid, &dispid);
   }
```

## <a name="see-also"></a>Ayrıca bkz.

- [IDispatchEx Arabirimi](../../winscript/reference/idispatchex-interface.md)
- [IDispatchEx::GetDispID](../../winscript/reference/idispatchex-getdispid.md)
- [IDispatchEx::DeleteMemberByName](../../winscript/reference/idispatchex-deletememberbyname.md)
- [IDispatchEx::DeleteMemberByDispID](../../winscript/reference/idispatchex-deletememberbydispid.md)