---
title: Idiadatasource::get_lasterror | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::get_lastError method
ms.assetid: cf08850b-8b75-4e8c-90bd-bd0214756f99
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3ad0570436dda6ac9ae52325c891b32a563cf6f7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788512"
---
# <a name="idiadatasourcegetlasterror"></a>IDiaDataSource::get_lastError
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Son yükleme hatası için dosya adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_lastError (  
   BSTR* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 pRetVal  
 [out] Son yükleme hatayla ilişkili .pdb dosyasının adını içeren bir dize döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir yükleme işlemi nedeniyle son hata kodunu döndürür. Döndürür `E_INVALIDARG` varsa `pRetVal` parametresi `NULL`.  
  
## <a name="example"></a>Örnek  
  
```cpp#  
BSTR    fileName;  
HRESULT errorCode = pSource->get_lastError( &fileName );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)
