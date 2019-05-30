---
title: SccHistory işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccHistory
helpviewer_keywords:
- SccHistory function
ms.assetid: a636d9d3-47c1-4b48-ac6b-bcfde19d6cf9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bad55b0fce5f4bec27ec707a4f9578c627a07363
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353611"
---
# <a name="scchistory-function"></a>SccHistory İşlevi
Bu işlev, belirtilen dosyaları geçmişini görüntüler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccHistory(
   LPVOID    pvContext,
   HWND      hWnd,
   LONG      nFiles,
   LPCSTR*   lpFileNames,
   LONG      fOptions,
   LPCMDOPTS pvOptions
);
```

#### <a name="parameters"></a>Parametreler
 `pvContext`

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 `hWnd`

[in] Kaynak Denetimi Eklentisi sağladığı herhangi bir iletişim kutusu için bir üst öğe olarak kullanabileceğiniz IDE penceresi için bir tanıtıcı.

 `nFiles`

[in] Belirtilen dosya sayısı `lpFileName` dizisi.

 `lpFileName`

[in] Dosyaların tam adları dizisi.

 `fOptions`

[in] Komut bayrakları (şu anda değil kullanılır).

 `pvOptions`

[in] Kaynak denetimi fişi özel seçenekleri.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Sürüm Geçmişi başarıyla alındı.|
|SCC_I_RELOADFILE|Diskteki dosyanın gerçekten değişiklik geçmişini getirilirken (örneğin, eski bir sürümünü alarak), kaynak denetim sistemi IDE bu dosyayı yeniden yüklemek için.|
|SCC_E_FILENOTCONTROLLED|Dosya kaynak denetimi altında değil.|
|SCC_E_OPNOTSUPPORTED|Kaynak denetim sistemi bu işlemi desteklemiyor.|
|SCC_E_NOTAUTHORIZED|Kullanıcı bu işlemi gerçekleştirmek için izin verilmiyor.|
|SCC_E_ACCESSFAILURE|Kaynak denetim sistemi, ağ veya çakışma sorunları nedeniyle muhtemelen erişilirken sorun oluştu. Bir yeniden deneme önerilir.|
|SCC_E_PROJNOTOPEN|Proje değiştirilmediğinden açılır.|
|SCC_E_NONSPECIFICERROR|Belirli olmayan hata oluştu. Dosya geçmişi alınamadı.|

## <a name="remarks"></a>Açıklamalar
 Kaynak denetimi eklentisi her dosyanın geçmişini görüntülemek için kendi iletişim kutusunu görüntüleyebilirsiniz kullanarak `hWnd` olarak üst pencere. Alternatif olarak, isteğe bağlı geri çağırma çıktıyı işlevi sağlanan için [SccOpenProject](../extensibility/sccopenproject-function.md) , destekleniyorsa, kullanılabilir.

 Belirli koşullar altında bu çağrı yürütülmesi sırasında incelenmekte olan dosyayı değiştirmek olduğunu unutmayın. Örneğin, [!INCLUDE[vsvss](../extensibility/includes/vsvss_md.md)] history komutu kullanıcı dosyanın eski bir sürümünü almak için bir fırsat sunar. Böyle bir durumda, kaynak denetimi eklentisi döndürür `SCC_I_RELOAD` dosyayı yeniden yüklemeniz gerekir IDE uyarır.

> [!NOTE]
> Kaynak denetimi eklentisi dosyaları dizisi için bu işlevi desteklemiyorsa, yalnızca ilk dosyası için dosya geçmişi görüntülenebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [SccOpenProject](../extensibility/sccopenproject-function.md)