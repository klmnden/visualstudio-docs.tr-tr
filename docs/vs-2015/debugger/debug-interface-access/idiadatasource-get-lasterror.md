---
title: Idiadatasource::get_lasterror | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::get_lastError method
ms.assetid: cf08850b-8b75-4e8c-90bd-bd0214756f99
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9c6824d651cc56aa56d027996abf6b76107adf30
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49303010"
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



