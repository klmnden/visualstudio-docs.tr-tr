---
title: IDebugModule3::GetSymbolInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugModule3::GetSymbolInfo
helpviewer_keywords:
- GetSymbolInfo method
- IDebugModule3::GetSymbolInfo method
ms.assetid: dda5e8e1-6878-4aa9-9ee4-e7d0dcc11210
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bd952242db8b7394fa8915319686ac431b84947d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323945"
---
# <a name="idebugmodule3getsymbolinfo"></a>IDebugModule3::GetSymbolInfo
Her yol arama sonuçlarını yanı sıra semboller için Aranan yol listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSymbolInfo(
    SYMBOL_SEARCH_INFO_FIELDS  dwFields,
    MODULE_SYMBOL_SEARCH_INFO* pInfo
);
```

```csharp
int GetSymbolInfo(
    enum_SYMBOL_SEARCH_INFO_FIELDS dwFields,
    MODULE_SYMBOL_SEARCH_INFO[]    pinfo
);
```

## <a name="parameters"></a>Parametreler
`dwFields`\
[in] Bayraklarının bir birleşimi [SYMBOL_SEARCH_INFO_FIELDS](../../../extensibility/debugger/reference/symbol-search-info-fields.md) hangi alanları belirten sabit listesi `pInfo` doldurulacak olan.

`pInfo`\
[out] A [MODULE_SYMBOL_SEARCH_INFO](../../../extensibility/debugger/reference/module-symbol-search-info.md) Yapı üyeleri olan belirtilen bilgileriyle doldurulacak. Bu bir null değeri ise, bu yöntemi döndürür `E_INVALIDARG`.

## <a name="return-value"></a>Dönüş Değeri
Yöntem başarılı olursa, döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

> [!NOTE]
> Döndürülen dize (içinde `MODULE_SYMBOL_SEARCH_INFO` yapısı) boş olabilir bile `S_OK` döndürülür. Bu durumda, geri dönmek için hiçbir arama bilgisi vardı.

## <a name="remarks"></a>Açıklamalar
Varsa `bstrVerboseSearchInfo` alanını `MODULE_SYMBOL_SEARCH_INFO` yapısı boş değil ve ardından arama yolları ve bu arama sonuçlarının bir listesini içerir. Listenin sonuca göre ve ardından üç nokta ("..."), ardından bir yol ile biçimlendirilir. Birden fazla yol sonuç çifti varsa, her bir çifti "\r\n" (satır başı-başı/satır besleme) çifti tarafından ayrılmış. Desen şöyle görünür:

\<yolu >... \<sonucu > \r\n\<yolu >... \<sonucu > \r\n\<yolu >... \<sonucu >

En son giriş \r\n dizisi yok unutmayın.

## <a name="example"></a>Örnek
Bu örnekte, üç farklı arama sonuçları ile üç yolları Bu yöntemi döndürür. Her satır, satır başı-başı/satır besleme çifti ile sonlandırılır. Örnek Çıktı, yalnızca tek bir dize olarak arama sonuçlarını yazdırır.

> [!NOTE]
> Bir durum hemen ardından "..." satırın sonuna kadar her şeyi sonucudur.

```cpp
void ShowSymbolSearchResults(IDebugModule3 *pIDebugModule3)
{
    MODULE_SYMBOL_SEARCH_INFO ssi = { 0 };
    HRESULT hr;
    hr = pIDebugModule3->GetSymbolInfo(SSIF_VERBOSE_SEARCH_INFO,&ssi);
    if (SUCCEEDED(hr)) {
        CComBSTR searchInfo = ssi.bstrVerboseSearchInfo;
        if (searchInfo.Length() != 0) {
            std::wcout << (wchar_t *)(BSTR)searchInfo;
            std::wcout << std::endl;
        }
    }
}
```

**c:\symbols\user32.pdb... Soubor nebyl nalezen. ** 
 **c:\winnt\symbols\user32.pdb... Sürüm eşleşmiyor. ** 
 ** \\\symbols\symbols\user32.dll\0a8sd0ad8ad\user32.pdb... Sembol yüklenmedi.**

## <a name="see-also"></a>Ayrıca bkz.

- [SYMBOL_SEARCH_INFO_FIELDS](../../../extensibility/debugger/reference/symbol-search-info-fields.md)
- [MODULE_SYMBOL_SEARCH_INFO](../../../extensibility/debugger/reference/module-symbol-search-info.md)
- [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)
