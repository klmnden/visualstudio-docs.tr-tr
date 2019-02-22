---
title: Idiadatasource::opensession | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::openSession method
ms.assetid: a3319ed0-3979-483b-9852-c0af96852c48
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 393abb3b1e1872a416865cbfee5c142bef98ce78
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56637080"
---
# <a name="idiadatasourceopensession"></a>IDiaDataSource::openSession
Semboller sorgulamak için bir oturum açar.

## <a name="syntax"></a>Sözdizimi

```C++
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

```C++
IDiaSession* pSession;
HRESULT hr = pSource->openSession( &pSession );
if (FAILED(hr))
{
   // report error
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)
- [Genel bakış](../../debugger/debug-interface-access/overview-debug-interface-access-sdk.md)
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [.Pdb Dosyasını Sorgulama](../../debugger/debug-interface-access/querying-the-dot-pdb-file.md)
