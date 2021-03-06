---
title: SccDiff işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccDiff
helpviewer_keywords:
- SccDiff function
ms.assetid: d49bc8c5-f631-4153-9d3c-feb3564da305
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 52da17cbb7f6349d99a04709bbe469501394d4e5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66327513"
---
# <a name="sccdiff-function"></a>SccDiff işlevi
Bu işlev görüntüler (veya isteğe bağlı olarak yalnızca denetler) geçerli dosya (yerel diskte) ile son iade sürümü arasındaki farkları kaynak denetim sistemi.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccDiff(
   LPVOID    pvContext,
   HWND      hWnd,
   LPCSTR    lpFileName,
   LONG      fOptions,
   LPCMDOPTS pvOptions
);
```

### <a name="parameters"></a>Parametreler
 pvContext

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 hWnd

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 lpFileName

[in] Fark istendiği dosya adı.

 fOptions

[in] Komut bayrakları. Açıklamalar, Ayrıntılar için bkz.

 pvOptions

[in] Kaynak denetimi fişi özel seçenekleri.

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Çalışma kopyasını ve sunucu sürümü aynıdır.|
|SCC_I_FILESDIFFERS|Kaynak denetimi altında sürüm çalışma kopyası farklıdır.|
|SCC_I_RELOADFILE|Bir dosya veya projenin yeniden yüklenmesi gerekiyor.|
|SCC_E_FILENOTCONTROLLED|Dosya kaynak denetimi altında değil.|
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata; Dosya farkı alınamadı.|
|SCC_E_FILENOTEXIST|Yerel dosya bulunamadı.|

## <a name="remarks"></a>Açıklamalar
 Bu işlev, iki farklı amaçlara hizmet eder. Varsayılan olarak, bir dosyaya değişikliklerin bir listesini görüntüler. Kaynak Denetimi Eklentisi, kullanıcının dosya diskte ve kaynak denetimi altındaki bir dosyayı en son sürümü arasındaki farkları görüntülemek için seçer herhangi bir biçimde kendi penceresi açılır.

 Alternatif olarak, IDE bir dosyanın değişip değişmediğini belirlemek yalnızca gerekebilir. Örneğin, IDE kullanıcı bildiren olmadan bir dosyayı kullanıma denetlemek güvenli olup olmadığını belirlemek gerekebilir. Bu durumda, IDE geçirir `SCC_DIFF_CONTENTS` bayrağı. Kaynak Denetimi Eklentisi diskte, kaynak-denetimli dosya bayt, dosyayı denetleyin ve kullanıcı için hiçbir şey görüntülemeden iki dosyayı farklı olup olmadığını gösteren bir değer döndürmesi gerekir.

 Performans iyileştirme, bir sağlama toplamı veya bir zaman damgası için çağıran bayt bayt karşılaştırma yerine göre alternatif kaynak denetimi eklentisi kullanabilir `SCC_DIFF_CONTENTS`: Bu formları karşılaştırma açıkça daha hızlı ancak daha az güvenilir. Tüm kaynak denetimi sistemlerini bu alternatif karşılaştırma yöntemleri destekleyebilir ve eklenti içeriğini karşılaştırma dönmesi gerekebilir. Tüm kaynak denetimi eklentileri en az bir içindekiler karşılaştırmayı desteklemesi gerekir.

> [!NOTE]
> Hızlı fark bayrakları birbirini dışlar. Bayrak geçirmek için geçerlidir, ancak aynı anda birden fazla geçirmek için geçerli değil. `SCC_DIFF_QUICK_DIFF`, test etmek için tüm bayrakları bir araya getiren bir maskesi olan kullanılabilir, ancak hiçbir zaman bir parametre olarak geçirilmelidir.

|`fOption`|Açıklama|
|---------------|-------------|
|SCC_DIFF_IGNORECASE|Büyük küçük harf duyarsız karşılaştırma (hızlı ya da visual fark için kullanılabilir).|
|SCC_DIFF_IGNORESPACE|(Hızlı ya da visual fark için kullanılabilir) boşluk yok sayar.|
|SCC_DIFF_QD_CONTENTS|Dosyanın bayt sessiz bir şekilde karşılaştırır.|
|SCC_DIFF_QD_CHECKSUM|Sessiz bir şekilde dosya desteklenen bir sağlama toplamı ile karşılaştırır. Desteklenmeyen, içindekiler karşılaştırma geri döner.|
|SCC_DIFF_QD_TIME|Sessiz bir şekilde dosya desteklendiğinde, zaman damgası ile karşılaştırır. Desteklenmeyen, içindekiler karşılaştırma geri döner.|

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)