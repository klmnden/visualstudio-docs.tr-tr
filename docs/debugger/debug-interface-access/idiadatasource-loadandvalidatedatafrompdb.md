---
title: Idiadatasource::loadandvalidatedatafrompdb | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaDataSource::loadAndValidateDataFromPdb method
ms.assetid: d66712dd-6c24-4192-919a-cce262066f0e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5426e27d7b100c42cd571935b1634d6dbd6e990f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62833553"
---
# <a name="idiadatasourceloadandvalidatedatafrompdb"></a>IDiaDataSource::loadAndValidateDataFromPdb
Açılır ve program veritabanı (.pdb) dosyası, sağlanan imza bilgileri eşleştiğini doğrular ve hata ayıklama veri kaynağı olarak .pdb dosyasını hazırlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT loadAndValidateDataFromPdb ( 
   LPCOLESTR pdbPath,
   GUID*     pcsig70,
   DWORD     sig,
   DWORD     age
);
```

#### <a name="parameters"></a>Parametreler
`pdbPath`

[in] .Pdb dosyasının yolu.

`pcsig70`

[in] .Pdb dosyası imzasını karşı GUID imzası. Yalnızca .pdb dosyaları [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] ve daha sonra GUID imzalara sahip olduğunu.

`sig`

[in] .Pdb dosyası imzasını karşı 32-bit imzası.

`age`

[in] Yaş değeri doğrulayın. Yaş herhangi bir bilinen bir saat değerine karşılık değil, bir .pdb dosyası ile ilgili bir .exe dosyası eşit olup olmadığını belirlemek için kullanılır.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Aşağıdaki tabloda, bu yöntem olası dönüş değerleri gösterir.

|Değer|Açıklama|
|-----------|-----------------|
|E_PDB_NOT_FOUND|Dosya açılamadı veya dosya geçersiz bir biçime sahip.|
|E_PDB_FORMAT|Bir dosya biçimi geçersiz erişme girişiminde bulunuldu.|
|E_PDB_INVALID_SIG|İmza ile eşleşmiyor.|
|E_PDB_INVALID_AGE|Yaş eşleşmiyor.|
|E_INVALIDARG|Geçersiz parametre.|
|E_UNEXPECTED|Veri kaynağı zaten hazırlandı.|

## <a name="remarks"></a>Açıklamalar
.Pdb dosyası, imza hem yaş değerler içeriyor. .Pdb dosyası ile eşleşen .exe veya .dll dosyasında bu değerleri çoğaltılır. Veri kaynağı hazırlamadan önce bu yöntem adlandırılmış .pdb dosyasının imza ve yaş sağlanan değerler eşleştiğini doğrular.

Doğrulama olmadan bir .pdb dosyası yüklemek için kullanın [Idiadatasource::loaddatafrompdb](../../debugger/debug-interface-access/idiadatasource-loaddatafrompdb.md) yöntemi.

(Bir geri dönüş mekanizması) veri yükleme işlemi için erişmek için kullandığı [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi.

Doğrudan bellekten bir .pdb dosyası yüklemek için kullanın [Idiadatasource::loaddatafromıstream](../../debugger/debug-interface-access/idiadatasource-loaddatafromistream.md) yöntemi.

## <a name="example"></a>Örnek

```C++
IDiaDataSource* pSource;  // Previously created data source.
DEFINE_GUID(expectedGUIDSignature,0x1234,0x5678,0x01,0x02,0x03,0x04,0x05,0x06,0x07,0x08);
DWORD expectedFileSignature = 0x12345678;
DWORD expectedAge           = 128;

HRESULT hr;
hr = pSource->loadAndValidateDataFromPdb( L"yprog.pdb",
                                          &expectedGUIDSignature,
                                          expectedFileSignature,
                                          expectedAge);
if (FAILED(hr))
{
    // Report an error
}

```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaDataSource](../../debugger/debug-interface-access/idiadatasource.md)
- [IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)
- [IDiaDataSource::loadDataFromPdb](../../debugger/debug-interface-access/idiadatasource-loaddatafrompdb.md)
- [IDiaDataSource::loadDataFromIStream](../../debugger/debug-interface-access/idiadatasource-loaddatafromistream.md)
