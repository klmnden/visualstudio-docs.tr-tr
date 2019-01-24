---
title: IDiaPropertyStorage::ReadLONG | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadLONG
ms.assetid: 32054cbc-db55-4513-a1b4-de80e77aac8a
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 08661272bea779ff0789619d58bf6f2837a21917
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786878"
---
# <a name="idiapropertystoragereadlong"></a>IDiaPropertyStorage::ReadLONG
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Okur `LONG` değerlerde özellik kümesi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT ReadDLONG (   
   PROPID id,  
   LONG*  pValue  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `id`  
 [in] Okunacak özellik tanımlayıcısı (`PROPID` WTypes.h tanımlanan bir `ULONG`).  
  
 `pValue`  
 [out] Özellik değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_INVALIDARG` özelliği türü değilse `LONG`.  
  
## <a name="remarks"></a>Açıklamalar  
 A `LONG` Windows 32-bit imzalı bir tamsayı olarak tanımlanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)
