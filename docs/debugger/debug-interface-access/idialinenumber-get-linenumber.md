---
title: Idialinenumber::get_linenumber | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_lineNumber method
ms.assetid: 2dff3fd9-097d-4645-bc1b-cb65ecbc42a6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 643c27b432a1770b78226a0471e6304f89a02092
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54977635"
---
# <a name="idialinenumbergetlinenumber"></a>IDiaLineNumber::get_lineNumber
Kaynak dosyadaki satır numarasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_lineNumber (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Satır numarası kaynak dosyada döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
  
```C++  
CComPtr< IDiaLineNumber> pLine;  
DWORD linenum;  
pLine->get_lineNumber( &linenum );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)