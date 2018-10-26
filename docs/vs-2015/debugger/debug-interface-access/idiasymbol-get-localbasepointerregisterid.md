---
title: Idiasymbol::get_localbasepointerregisterıd | Microsoft Docs
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
- IDiaSymbol::get_localBasePointerRegisterId method
ms.assetid: 9cbcaf00-9ace-45e1-b164-7a9439e08083
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0f0201e062d0106e297c128c71c22dadf43a7890
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49860571"
---
# <a name="idiasymbolgetlocalbasepointerregisterid"></a>IDiaSymbol::get_localBasePointerRegisterId
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yerel değişkenler yığında için temel bir işaretçi tutan kayıt Kimliğini alır. Şu durumlarda kullanın [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) ayarlanır `SymTagFunction`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_localBasePointerRegisterId (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Yerel değişkenler yığında için temel bir işaretçi tutan kayıt Kimliğini döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: Dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



