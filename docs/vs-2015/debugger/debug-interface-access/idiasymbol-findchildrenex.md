---
title: IDiaSymbol::findChildrenEx | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::findChildrenEx
ms.assetid: 6e045045-da8c-4338-9423-81a1ca20c405
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0ee0ee9938ba2529afd7ea437c56761e1768e8cd
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "68150005"
---
# <a name="idiasymbolfindchildrenex"></a>IDiaSymbol::findChildrenEx
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Alt simge alır. Program üzerinde iyileştirme ile derlenmişse döndürülen yerel semboller dinamik aralık bilgiler içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findChildrenEx (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
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
  
 `ppResult`  
 [out] Döndürür bir [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md) alt simge listesini içeren bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` simgenin en az bir alt öğe bulunamadı ya da döndürür `S_FALSE` alt öğe bulundu; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem genişletilmiş sürümüdür [Idiasymbol::findchildren](../../debugger/debug-interface-access/idiasymbol-findchildren.md).  
  
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
