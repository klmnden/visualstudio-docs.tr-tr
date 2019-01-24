---
title: IDiaSymbol::findChildrenExByAddr | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::findChildrenExByAddr
ms.assetid: c1e7885d-2d15-4529-9ac2-32dd22efe31c
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8f791074d029be78eb7d45e06dce8a8cce145f71
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54757843"
---
# <a name="idiasymbolfindchildrenexbyaddr"></a>IDiaSymbol::findChildrenExByAddr
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirli bir adreste geçerli olan alt simge alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findChildrenExByAddr (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   DWORD             address,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `symtag`  
 [in] Alınacak, alt simge etiketleri sınıfında tanımlandığı gibi belirtir [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md). Kümesine `SymTagNull` alınacak tüm alt öğeleri için.  
  
 `name`  
 [in] Alınacak alt adını belirtir. Kümesine `NULL` alınacak tüm alt öğeleri için.  
  
 `compareFlags`  
 [in] Ad eşleştirme için uygulanacak karşılaştırma seçeneklerini belirtir. Değerlerini [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md) numaralandırma, tek başına veya birlikte kullanılabilir.  
  
 `address`  
 [in] Simgenin adresi.  
  
 `ppResult`  
 [out] Döndürür bir [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md) alt simge listesini içeren bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` simgenin en az bir alt öğe bulunamadı ya da döndürür `S_FALSE` alt öğe bulundu; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Döndürülen yerel semboller dinamik aralık bilgilerini içerir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md)   
 [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [Idiasession::findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md)   
 [NameSearchOptions Numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md)
