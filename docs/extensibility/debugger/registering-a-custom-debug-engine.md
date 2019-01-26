---
title: Hata ayıklama motoru özel bir kaydetme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, registering
ms.assetid: 9984cd3d-d34f-4662-9ace-31766499abf5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3f403b18175e486dad40166d1b48960fe7b2bed2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996486"
---
# <a name="register-a-custom-debug-engine"></a>Bir özel hata ayıklama altyapısını kaydetme
Hata ayıklama altyapısı gereken kendisini aşağıdaki COM kuralları bir sınıf üreteci kaydetmek yanı sıra Visual Studio kayıt defteri alt anahtarı Visual Studio ile kaydedin.  
  
> [!NOTE]
>  Hata ayıklama altyapısının bir parçası olarak oluşturulan TextInterpreter örnek kaydetmek nasıl bir örnek bulabilirsiniz [Öğreticisi: ATL COM kullanarak bir hata ayıklama altyapısı oluşturma](https://msdn.microsoft.com/library/9097b71e-1fe7-48f7-bc00-009e25940c24).  
  
## <a name="dll-server-process"></a>DLL sunucu işlemi  
 Hata ayıklama altyapısı genellikle kendi DLL'de bir COM sunucusu olarak ayarlanır. Visual Studio erişebilmeniz için önce bu nedenle, hata ayıklama altyapısı kendi sınıf üreteci CLSID değeri COM ile kaydetmeniz gerekir. Ardından, hata ayıklama altyapısı kendisini herhangi bir özelliği (Aksi ölçümler olarak bilinen) oluşturmak için Visual Studio ile hata ayıklama kaydetmelisiniz altyapısını destekler. Visual Studio kayıt defteri alt anahtarına yazılan ölçümler seçimi, hata ayıklama altyapısı destekler özelliklerine bağlıdır.  
  
 [Hata ayıklama için SDK Yardımcıları](../../extensibility/debugger/reference/sdk-helpers-for-debugging.md) yalnızca bir hata ayıklama altyapısı; kaydetmek gerekli kayıt defteri konumlarını açıklar da açıklar *dbgmetric.lib* birçok kullanışlı işlevi ve bildirimleri içeren kitaplığı oluşturan C++ geliştiricileri için daha kolay bir şekilde kayıt defterini düzenleme.  
  
### <a name="example"></a>Örnek  
 Aşağıdaki örnek (TextInterpreter örnekten) nasıl kullanılacağını gösterir `SetMetric` işlevi (gelen *dbgmetric.lib*), Visual Studio ile hata ayıklama altyapısı kaydedilecek. Geçirilen ölçümler de tanımlanan *dbgmetric.lib*.  
  
> [!NOTE]
>  TextInterpreter temel hata ayıklama altyapısıdır; Bunu ayarlanmamış — ve bu nedenle kaydetme — diğer tüm özellikler. Daha eksiksiz bir hata ayıklama altyapısı tam bir listesi gerekir `SetMetric` çağrıları veya eşdeğeri, hata ayıklama altyapısı her bir özellik için bir tane destekler.  
  
```  
// Define base registry subkey to Visual Studio.  
static const WCHAR strRegistrationRoot[] = L"Software\\Microsoft\\VisualStudio\\8.0";  
  
HRESULT CTextInterpreterModule::RegisterServer(BOOL bRegTypeLib, const CLSID * pCLSID)  
{  
    SetMetric(metrictypeEngine, __uuidof(Engine), metricName, L"Text File", false, strRegistrationRoot);  
    SetMetric(metrictypeEngine, __uuidof(Engine), metricCLSID, CLSID_Engine, false, strRegistrationRoot);  
    SetMetric(metrictypeEngine, __uuidof(Engine), metricProgramProvider, CLSID_MsProgramProvider, false, strRegistrationRoot);  
  
    return base::RegisterServer(bRegTypeLib, pCLSID);  
}  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)   
 [Hata ayıklama için SDK Yardımcıları](../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)   
 [Öğretici: ATL COM kullanarak bir hata ayıklama altyapısı oluşturma](https://msdn.microsoft.com/library/9097b71e-1fe7-48f7-bc00-009e25940c24)