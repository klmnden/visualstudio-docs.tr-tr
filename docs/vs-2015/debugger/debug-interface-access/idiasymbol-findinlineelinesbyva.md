---
title: IDiaSymbol::findInlineeLinesByVA | Microsoft Docs
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
ms.assetid: 61427d33-30d2-4ac9-9bd6-c58c6c705072
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6a82df12d28c29d095b67cb4b36eb988238b5485
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49886038"
---
# <a name="idiasymbolfindinlineelinesbyva"></a>IDiaSymbol::findInlineeLinesByVA
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir istemci doğrudan veya dolaylı olarak bu sembol belirtilen sanal adres (VA) içinde satır içine alınmış, bulunan tüm işlevlerin satır numarası bilgisi yinelemek sağlayan bir sabit listesi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findInlineeLinesByVA (   
   ULONGLONG             va,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `va`  
 [in] Bir VA. adresini belirtir  
  
 `length`  
 [in] Adres aralığı, bu sorguyu kapsayacak şekilde bayt sayısını belirtir.  
  
 `ppResult`  
 [out] Tutan bir `IDiaEnumLineNumbers` alınan satır numaraları listesi içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md)   
 [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)



