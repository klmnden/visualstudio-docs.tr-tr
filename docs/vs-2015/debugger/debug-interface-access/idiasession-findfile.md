---
title: Idiasession::findfile | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findFile method
ms.assetid: a215dc21-b316-40d7-9923-55bfa014976b
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1e791bc09ba3dd4f1811c650926eadb0f7f0462a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54778140"
---
# <a name="idiasessionfindfile"></a>IDiaSession::findFile
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Derlenecek dosya ve ada göre kaynak dosyaları alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findFile (   
   IDiaSymbol*           pCompiland,  
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSourceFiles** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCompiland`  
 [in] Bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) arama bağlamı olarak kullanılacak derlenecek temsil eden nesne. Bu parametre kümesine `NULL` kaynak dosyaları tüm derleme bulunamıyor.  
  
 `name`  
 [in] Alınacak kaynak dosyasının adını belirtir. Bu parametre kümesine `NULL` tüm kaynak dosyaları alınacak.  
  
 `option`  
 [in] Ad arama uygulanan karşılaştırma seçeneklerini belirtir. Değerlerini [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md) numaralandırma, tek başına veya birlikte kullanılabilir.  
  
 `ppResult`  
 [out] Döndürür bir [Idiaenumsourcefiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md) kaynak dosyaların listesini içeren bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
  
```cpp#  
IDiaEnumSourceFiles* pEnum;  
pSession->findFile( NULL, L"sourcefile.cpp", nsFNameExt, &pEnum );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumsourcefiles](../../debugger/debug-interface-access/idiaenumsourcefiles.md)   
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [NameSearchOptions Numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md)
