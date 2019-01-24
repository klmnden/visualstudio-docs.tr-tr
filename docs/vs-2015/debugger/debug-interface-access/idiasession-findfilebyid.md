---
title: Idiasession::findfilebyıd | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findFileById method
ms.assetid: 710efe04-78b5-4f3e-a1d8-f9b069063503
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3c57072d4b8707136f0ccd2a759bc3d393720efb
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771657"
---
# <a name="idiasessionfindfilebyid"></a>IDiaSession::findFileById
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir kaynak dosyası, kaynak dosya tanımlayıcısı tarafından alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findFileById (   
   DWORD            uniqueId,  
   IDiaSourceFile** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `uniqueId`  
 [in] Kaynak dosya tanımlayıcısını belirtir.  
  
 `ppResult`  
 [out] Döndürür bir [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) kaynak dosyasını temsil eden bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Kaynak dosya tanımlayıcısı, dahili olarak DIA SDK, tüm kaynak dosyaları benzersiz hale getirmek için kullanılan benzersiz bir değerdir. Bu yöntem genellikle DIA SDK'SININ dahili olarak kullanılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasession::findfile](../../debugger/debug-interface-access/idiasession-findfile.md)   
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)
