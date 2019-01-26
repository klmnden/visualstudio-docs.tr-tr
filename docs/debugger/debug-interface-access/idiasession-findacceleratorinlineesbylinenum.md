---
title: IDiaSession::findAcceleratorInlineesByLinenum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 386c87aa-f7b2-4d38-9dd6-fffba9ff01f0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9d963763f341430c92810fe811144212d2cc522e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999723"
---
# <a name="idiasessionfindacceleratorinlineesbylinenum"></a>IDiaSession::findAcceleratorInlineesByLinenum
Belirtilen kaynak konum için karşılık gelen satır içi çerçeveler için semboller numaralandırmasını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findAcceleratorInlineeLinesByName (   
   IDiaSymbol*           parent,  
   IDiaSourceFile*       file,  
   DWORD                 linenum,  
   DWORD                 colnum,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `parent`  
 [in] Bir `IDiaSymbol` aranacak gereken Hızlandırıcı saplama işlevi karşılık gelir.  
  
 `file`  
 [in] `IDiaSourceFile` Kaynak konum.  
  
 `linenum`  
 [in] Kaynak konumun satır numarası.  
  
 `colnum`  
 [in] Kaynak konumun sütun numarası.  
  
 `ppResult`  
 [out] Bir işaretçi bir `IDiaEnumLineNumbers` sonucu ile başlatılmış bir arabirim işaretçisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)