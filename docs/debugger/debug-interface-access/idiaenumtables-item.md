---
title: Idiaenumtables::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Item method
ms.assetid: d65ab262-10c6-48ce-95a3-b5e4cb2c85af
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6321b6bc651778e9d3aff7257a251eff6493f397
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53966148"
---
# <a name="idiaenumtablesitem"></a>IDiaEnumTables::Item
Bir dizin veya ad ile bir tabloyu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT Item (   
   VARIANT     index,  
   IDiaTable** table  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `index`  
 [in] Dizin veya adını [Idiatable](../../debugger/debug-interface-access/idiatable.md) alınacak. Bir tamsayı değişken kullandıysanız, aralığı 0 olmalıdır `count`-1, burada `count` tarafından döndürülen [Idiaenumtables::get_Count](../../debugger/debug-interface-access/idiaenumtables-get-count.md) yöntemi.  
  
 `table`  
 [out] Döndürür bir [Idiatable](../../debugger/debug-interface-access/idiatable.md) istediğiniz tabloyu temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir dize değişken belirtilirse, dize belirli bir tablo adları. Adı bir tablo adlarının sınıfında tanımlandığı gibi olmalıdır [sabitler (arabirim erişimi SDK'ı hata ayıklama)](../../debugger/debug-interface-access/constants-debug-interface-access-sdk.md).  
  
## <a name="example"></a>Örnek  
  
```C++  
VARIANT var;  
var.vt = VT_BSTR;  
var.bstrVal = SysAllocString(DiaTable_Symbols );  
IDiaTable* pTable;  
pEnumTables->Item( var, &pTable );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumtables](../../debugger/debug-interface-access/idiaenumtables.md)   
 [Idiatable](../../debugger/debug-interface-access/idiatable.md)   
 [Idiaenumtables::get_Count](../../debugger/debug-interface-access/idiaenumtables-get-count.md)   
 [Sabitler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/constants-debug-interface-access-sdk.md)