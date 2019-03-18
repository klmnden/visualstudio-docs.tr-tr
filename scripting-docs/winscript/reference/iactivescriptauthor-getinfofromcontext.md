---
title: IActiveScriptAuthor::GetInfoFromContext | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptAuthor.GetInfoFromContext
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptAuthor::GetInfoFromContext
ms.assetid: 9891b095-6eb5-4473-87c0-c2e5cd2afc1a
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e4fe885e116019608dd8d748c3cbdaff5d31dd2a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58154419"
---
# <a name="iactivescriptauthorgetinfofromcontext"></a>IActiveScriptAuthor::GetInfoFromContext
Döndürür bir kod bloğu içinde bilgi ve belirli bir karakter için yer işareti konumlarını yazın. Bu üye için bilgi IntelliSense, genel listeler ve parametre ipuçları sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetInfoFromContext(  
   LPCOLESTR  pszCode,  
   ULONG      cchCode,  
   ULONG      ichCurrentPosition,  
   DWORD      dwListTypesRequested,  
   DWORD      *pdwListTypesProvided,  
   ULONG      *pichListAnchorPosition,  
   ULONG      *pichFuncAnchorPosition,  
   MEMBERID   *pmemid,  
   LONG       *piCurrentParameter,  
   IUnknown   **ppunk  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszCode`  
 [in] Bilgi sonuçları oluşturmak için kullanılan kod bloğu dizesi adresi.  
  
 `cchCode`  
 [in] Kod bloğunun uzunluğu.  
  
 `ichCurrentPosition`  
 [in] Bloğun başlangıç göre karakterin konumu.  
  
 `dwListTypesRequested`  
 [in] İstenen liste türleri. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-----------------|  
|SCRIPT_CMPL_NOLIST|0x0000|Liste yok.|  
|SCRIPT_CMPL_MEMBERLIST|0x0001|Üye listesi.|  
|SCRIPT_CMPL_ENUMLIST|0x0002|Numaralandırma listesi.|  
|SCRIPT_CMPL_PARAMLIST|0x0004|Yöntem parametresi listesinden çağırın.|  
|SCRIPT_CMPL_GLOBALLIST|0x0008|Genel liste.|  
  
 SCRIPT_CMPL_GLOBALLIST türü ile diğer tamamlama öğeleri OR işlecini kullanarak birleştirilebilir varsayılan bir tamamlanma öğesi olarak kabul edilir. Diğer tamamlanma listesi öğeleri için tür bilgilerini doldurmak betik altyapısı ilk yazma çalışır. Bu başarısız olursa altyapısı için SCRIPT_CMPL_GLOBALLIST doldurur.  
  
 `pdwListTypesProvided`  
 [out] Sağlanan liste türü.  
  
 `pichListAnchorPosition`  
 [out] Geçerli konumu içeren bağlamı başlangıç dizini. Bloğun başlangıcını göreli Başlangıç dizinidir.  
  
 Bu doldurulur yalnızca `dwListTypesRequested` SCRIPT_CMPL_MEMBERLIST, SCRIPT_CMPL_ENUMLIST veya SCRIPT_CMPL_GLOBALLIST içerir. Diğer istenen liste türleri için sonuç tanımsızdır.  
  
 `pichFuncAnchorPosition`  
 [out] Geçerli konumu içeren işlev çağrısı başlangıç dizini. Bloğun başlangıcını göreli Başlangıç dizinidir.  
  
 Bu yalnızca geçerli konumunu içeren bir işlev çağrısı bağlamımızdır ve zamanı doldurulur `dwListTypesRequested` SCRIPT_CMPL_PARAMLIST içerir. Aksi halde sonuç tanımsızdır.  
  
 `pmemid`  
 [out] Bir türü tarafından tanımlandığı gibi işlevinin MEMBERID `IProvideMultipleClassInfo``ppunk` çıkış parametresi.  
  
 Bu doldurulur yalnızca `dwListTypesRequested` SCRIPT_CMPL_PARAMLIST içerir.  
  
 `piCurrentParameter`  
 [out] Geçerli konumu içeren parametrenin dizini. Geçerli konum işlev adına, -1 döndürülür.  
  
 `piCurrentParameter` Değeri doldurulur yalnızca `dwListTypesRequested` SCRIPT_CMPL_PARAMLIST içerir.  
  
 `ppunk`  
 Biçiminde sağlanan tür bilgilerini bir `IProvideMultipleClassInfo` nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IProvideMultipleClassInfo arabirimi](https://docs.microsoft.com/dotnet/api/microsoft.visualstudio.ole.interop.iprovidemultipleclassinfo)   
 [IActiveScriptAuthor Arabirimi](../../winscript/reference/iactivescriptauthor-interface.md)