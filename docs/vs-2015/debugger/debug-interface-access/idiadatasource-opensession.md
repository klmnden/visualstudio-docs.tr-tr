---
title: Idiadatasource::opensession | Microsoft Docs
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
- IDiaDataSource::openSession method
ms.assetid: a3319ed0-3979-483b-9852-c0af96852c48
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bf4dc2e7dd7f0f8596efdd835aa1b1d9c809295c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49225855"
---
# <a name="idiadatasourceopensession"></a>IDiaDataSource::openSession
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Semboller sorgulamak için bir oturum açar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT openSession (   
   IDiaSession** ppSession  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 ppSession  
 [out] Döndürür bir [Idiasession](../../debugger/debug-interface-access/idiasession.md) Oturum Aç'ı temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Aşağıdaki tabloda, bu yöntem olası dönüş değerleri gösterir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|E_UNEXPECTED|[Idiadatasource](../../debugger/debug-interface-access/idiadatasource.md) nesne daha önce başlatılmamış bir simge kaynağı ile.|  
|E_INVALIDARG|Geçersiz `ppSession` parametresi.|  
|E_OUTOFMEMORY|Oturum açmak için bellek yetersiz.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem açılan bir [Idiasession](../../debugger/debug-interface-access/idiasession.md) bir veri kaynağı için nesne.  
  
 `IDiaSession` nesneleri sorgular veri kaynağına uygulayın. Bir oturum her kümesi, hata ayıklama sembolleri için bir adres alanı yönetir. Veri kaynağı simgeleri tarafından açıklanan .exe veya .dll dosyası ise (örneğin, birden çok işlem yüklü olması nedeniyle) etkin durumda birden çok adres aralıkları ve tek bir oturum için her bir adres aralığı kullanılmalıdır.  
  
## <a name="example"></a>Örnek  
  
```cpp#  
IDiaSession* pSession;  
HRESULT hr = pSource->openSession( &pSession );  
if (FAILED(hr))  
{  
   // report error  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiadatasource](../../debugger/debug-interface-access/idiadatasource.md)   
 [Genel bakış](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)   
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [.Pdb Dosyasını Sorgulama](../../debugger/debug-interface-access/querying-the-dot-pdb-file.md)



