---
title: QUERYCHANGESFUNC | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- QUERYCHANGESFUNC
helpviewer_keywords:
- QUERYCHANGESFUNC callback function
- QUERYCHANGESDATA structure
ms.assetid: 9d383e2c-eee1-4996-973a-0652d4c5951c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8ac0003d26296a25659debbab3352e4e37cbf2ec
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66334403"
---
# <a name="querychangesfunc"></a>QUERYCHANGESFUNC
Bu, bir geri çağırma işlevi tarafından kullanılan [SccQueryChanges](../extensibility/sccquerychanges-function.md) dosya adları topluluğu numaralandırır ve her bir dosyanın durumunu belirlemek için işlem.

 `SccQueryChanges` İşlevi işaretçisi ve dosyaların listesini verilen `QUERYCHANGESFUNC` geri çağırma. Kaynak Denetimi Eklentisi, belirli bir liste üzerinde numaralandırır ve listedeki her dosya için durum (Bu geri çağırma) aracılığıyla sağlar.

## <a name="signature"></a>İmza

```cpp
typedef BOOL (*QUERYCHANGESFUNC)(
   LPVOID pvCallerData,
   QUERYCHANGESDATA * pChangesData
);
```

## <a name="parameters"></a>Parametreler
 pvCallerData

[in] `pvCallerData` Parametresi için (IDE) çağıran tarafından geçirilen [SccQueryChanges](../extensibility/sccquerychanges-function.md). Kaynak Denetimi Eklentisi bu değerinin içeriği hakkında hiçbir varsayım olmanız gerekir.

 pChangesData

[in] İşaretçi bir [QUERYCHANGESDATA yapısı](#LinkQUERYCHANGESDATA) yapısını açıklayan bir dosyada yapılan değişiklikler.

## <a name="return-value"></a>Dönüş değeri
 IDE uygun hata kodu döndürür:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|İşleme devam edin.|
|SCC_I_OPERATIONCANCELED|İşlemeyi durdur.|
|SCC_E_xxx|Herhangi bir uygun SCC hata işleme durdurmanız gerekir.|

## <a name="LinkQUERYCHANGESDATA"></a> QUERYCHANGESDATA yapısı
 Her dosya için geçirilen yapısı aşağıdaki gibi görünür:

```cpp
struct QUERYCHANGESDATA_A
{
    DWORD  dwSize;
    LPCSTR lpFileName;
    DWORD  dwChangeType;
    LPCSTR lpLatestName;
};

typedef struct QUERYCHANGESDATA_A QUERYCHANGESDATA;

struct QUERYCHANGESDATA_W
{
    DWORD   dwSize;
    LPCWSTR lpFileName;
    DWORD   dwChangeType;
    LPCWSTR lpLatestName;
};
```

 Boyut (bayt cinsinden) bu yapının dwSize.

 lpDosyaAdı bu öğenin özgün dosya adı.

 dwChangeType dosyanın belirten bir durum kodu:

|Kod|Açıklama|
|----------|-----------------|
|`SCC_CHANGE_UNKNOWN`|Nelerin değiştiğini bildiremez.|
|`SCC_CHANGE_UNCHANGED`|Bu dosya için ad değişikliği yok.|
|`SCC_CHANGE_DIFFERENT`|Dosya farklı bir kimlik ile ancak veritabanında aynı adı yok.|
|`SCC_CHANGE_NONEXISTENT`|Dosya veritabanında veya yerel olarak mevcut değil.|
|`SCC_CHANGE_DATABASE_DELETED`|Dosya, veritabanında silindi.|
|`SCC_CHANGE_LOCAL_DELETED`|Dosya yerel olarak silindi ancak dosyayı veritabanında devam eder. Bu belirlenemiyorsa dönüş `SCC_CHANGE_DATABASE_ADDED`.|
|`SCC_CHANGE_DATABASE_ADDED`|Dosya veritabanına eklenen ancak yerel olarak mevcut değil.|
|`SCC_CHANGE_LOCAL_ADDED`|Dosya, veritabanında mevcut değil ve yeni bir yerel dosya.|
|`SCC_CHANGE_RENAMED_TO`|Dosya yeniden adlandırılmış veya taşınmış veritabanında `lpLatestName`.|
|`SCC_CHANGE_RENAMED_FROM`|Dosya yeniden adlandırılmış veya taşınmış veritabanı `lpLatestName`; izlemek, çok pahalı ise dönüş farklı bir bayrak gibi `SCC_CHANGE_DATABASE_ADDED`.|

 lpLatestName bu öğe için geçerli dosya adı.

## <a name="see-also"></a>Ayrıca bkz.
- [IDE tarafından uygulanan geri çağırma işlevleri](../extensibility/callback-functions-implemented-by-the-ide.md)
- [SccQueryChanges](../extensibility/sccquerychanges-function.md)
- [Hata kodları](../extensibility/error-codes.md)