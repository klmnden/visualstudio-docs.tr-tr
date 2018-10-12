---
title: IDebugCustomViewer::DisplayValue | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugCustomViewer::DisplayValue
helpviewer_keywords:
- IDebugCustomViewer::DisplayValue
ms.assetid: 7a538248-5ced-450e-97cd-13fabe35fb1c
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5c653e1c199e1007f62fd423f646042e629a2318
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49301294"
---
# <a name="idebugcustomviewerdisplayvalue"></a>IDebugCustomViewer::DisplayValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, belirtilen değeri görüntülemek için çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT DisplayValue(  
   HWND             hwnd,  
   DWORD            dwID,  
   IUnknown *       pHostServices,  
   IDebugProperty3* pDebugProperty);  
);  
```  
  
```csharp  
int DisplayValue(  
   IntPtr          hwnd,   
   uint            dwID,   
   object          pHostServices,   
   IDebugProperty3 pDebugProperty  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `hwnd`  
 [in] Ana penceresi  
  
 `dwID`  
 [in] Birden fazla tür destekleyen özel görüntüleyiciler kimliği.  
  
 `pHostServices`  
 [in] Ayrılmış. Her zaman null.  
  
 `pDebugProperty`  
 [in] Görüntülenecek değerini almak için kullanılan arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem gerekli penceresi oluştur, değerini görüntülemek, giriş bekle ve, tüm çağırana döndürmeden önce pencereyi görüntüle "modal" olmamasıdır. Başka bir deyişle, yöntem özelliğin değeri, bir pencere yok etme için kullanıcı girişini beklerken için çıktı penceresini oluşturmasını görüntüleme tüm yönlerini işlemesi gerekir.  
  
 Değer değiştirme desteklemek için verilen [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) nesne kullanabileceğiniz [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md) yöntemi — değeri bir dize olarak ifade edilebilir değilse. Aksi takdirde, özel arabirim oluşturmak gerekli olan — bunu uygulama ifade değerlendiricisi özel `DisplayValue` yöntemi — uygulayan aynı nesne üzerinde `IDebugProperty3` arabirimi. Bu özel arabirim yöntemleri bir rastgele boyut ve karmaşıklıktaki verileri değiştirmek için sağlamanız.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCustomViewer](../../../extensibility/debugger/reference/idebugcustomviewer.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md)

