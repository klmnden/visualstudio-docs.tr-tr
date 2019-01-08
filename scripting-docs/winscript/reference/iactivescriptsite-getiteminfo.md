---
title: IActiveScriptSite::GetItemInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.GetItemInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_GetItemInfo
ms.assetid: f859ed3b-02c1-4924-99f8-5f5bf1bf8405
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f4dc6515d64406870ca10f003d7cea515c49b7d8
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54095894"
---
# <a name="iactivescriptsitegetiteminfo"></a>IActiveScriptSite::GetItemInfo
İle eklenen bir öğe hakkında bilgi almak komut dosyası altyapısı sağlayan [IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetItemInfo(  
    LPCOLESTR pstrName,     // address of item name  
    DWORD dwReturnMask,     // bit mask for information retrieval  
    IUnknown **ppunkItem,   // address of pointer to item's IUnknown  
    ITypeInfo **ppTypeInfo  // address of pointer to item's ITypeInfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrName`  
 [in] Belirtilen öğe ile ilişkili adı [IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md) yöntemi.  
  
 `dwReturnMask`  
 [in] Öğesinin hangi bilgilerini döndürülmesi gerektiğini belirten bir bit maskesi. Komut dosyası altyapısı en az miktarda bilgi mümkün olduğundan istemelidir bazı dönüş parametreler (örneğin, `ITypeInfo`) yüklemek veya oluşturmak için önemli miktarda zaman alabilir. Aşağıdaki değerlerin bir birleşimi olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTINFO_IUNKNOWN|Döndürür `IUnknown` bu öğe için arabirim.|  
|SCRIPTINFO_ITYPEINFO|Döndürür `ITypeInfo` bu öğe için arabirim.|  
  
 `ppunkItem`  
 [out] Bir işaretçiye alan değişkenin adresini `IUnknown` verilen öğeyle ilişkili arabirimi. Komut dosyası altyapısı kullanabilirsiniz `IUnknown::QueryInterface` elde etmek için yöntemi `IDispatch` öğe için arabirim. Bu parametre NULL ise alan `dwReturnMask` SCRIPTINFO_IUNKNOWN değeri içermez. Ayrıca, öğe adı ile ilişkili hiçbir nesne yoksa NULL alır. Bu mekanizma kümesinde SCRIPTITEM_CODEONLY bayrağıyla adlandırılmış öğe eklendiğinde, basit bir sınıf oluşturmak için kullanılan [IActiveScript::AddNamedItem](../../winscript/reference/iactivescript-addnameditem.md) yöntemi.  
  
 `ppTypeInfo`  
 [out] Bir işaretçiye alan değişkenin adresini `ITypeInfo` öğeyle ilişkili arabirimi. Bu parametre NULL ise alan `dwReturnMask` SCRIPTINFO_ITYPEINFO değeri içermez veya bu öğe için tür bilgileri kullanılamıyor. Tür bilgileri kullanılabilir değil, olay kaynağı nesnesi olamaz ve ad bağlaması gerçekleşen, ile `IDispatch::GetIDsOfNames` yöntemi. Unutmayın `ITypeInfo` alınan arabirimi nesnesi birden fazla arabirim ve olay arabirimleri destekleyebilir çünkü öğenin coclass'ı (TKIND_COCLASS) açıklanmaktadır. Öğe destekliyorsa `IProvideMultipleTypeInfo` arabirimi `ITypeInfo` alınan arabirimidir aynı dizin sıfır olarak `ITypeInfo` , elde edilebilir kullanarak `IProvideMultipleTypeInfo::GetInfoOfIndex` yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`TYPE_E_ELEMENTNOTFOUND`|Belirtilen adda bir öğe bulunamadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem yalnızca tarafından gösterilen bilgileri alır `dwReturnMask` parametre; Bunun yapılması performansı artırır. Örneğin, bir `ITypeInfo` arabirimi bir öğe için gerekli değildir, bu yalnızca belirtilmedi `dwReturnMask`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)