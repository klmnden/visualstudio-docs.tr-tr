---
title: Idiasession::getenumtables | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::getEnumTables method
ms.assetid: 66e0fba2-ca63-4e24-a46a-c99c7fb61dd1
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f2659fa3e5c82e48092c9f2b4b009b7e82e72123
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53889539"
---
# <a name="idiasessiongetenumtables"></a>IDiaSession::getEnumTables
Sembol deposu içerisinde bulunan tüm tablolar için bir numaralandırıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT getEnumTables (   
   IDiaEnumTables** ppEnumTables  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnumTables`  
 [out] Döndürür bir [Idiaenumtables](../../debugger/debug-interface-access/idiaenumtables.md) nesne. Bu arabirim, sembol deposundaki tablolar numaralandırmak için kullanın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
 Bu örnekte kullanan genel bir işlev sunar `getEnumTables` belirli Numaralandırıcı nesnesi elde etmek için yöntemi. Numaralandırıcı bulunursa, işlev istendiği arayüz dönüştürülebilen bir işaretçi döndürür; Aksi halde, işlev döndürür `NULL`.  
  
```C++  
IUnknown *GetTable(IDiaSession *pSession, REFIID iid)  
{  
    IUnknown *pUnknown = NULL;  
    if (pSession != NULL)  
    {  
        CComPtr<IDiaEnumTables> pEnumTables;  
        if (pSession->getEnumTables(&pEnumTables) == S_OK)  
        {  
             CComPtr<IDiaTable> pTable;  
             DWORD celt = 0;  
             while(pEnumTables->Next(1,&pTable,&celt) == S_OK &&  
                   celt == 1)  
             {  
                  if (pTable->QueryInterface(iid, (void **)pUnknown) == S_OK)  
                  {  
                       break;  
                  }  
                  pTable = NULL;  
             }  
        }  
    }  
    return(pUnknown);  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumtables](../../debugger/debug-interface-access/idiaenumtables.md)   
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)