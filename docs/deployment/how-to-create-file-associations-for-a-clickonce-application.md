---
title: 'Nasıl yapılır: ClickOnce uygulaması Için dosya Ilişkilendirmeleri oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- file associations, ClickOnce applications
- ClickOnce deployment, file associations
ms.assetid: 835230c8-3177-440f-85e3-e40f1d8b4f9d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0526351d2b3e2c223aacbe0e58d9ee39bd1b19c4
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68924552"
---
# <a name="how-to-create-file-associations-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce uygulaması için dosya ilişkilendirmeleri oluşturma
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]uygulamalar bir veya daha fazla dosya adı uzantısıyla ilişkilendirilebilen için, Kullanıcı bu türden bir dosya açtığında uygulamanın otomatik olarak başlatılması gerekir. Bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamaya dosya adı uzantısı desteği eklemek basittir.

### <a name="to-create-file-associations-for-a-clickonce-application"></a>ClickOnce uygulaması için dosya ilişkilendirmeleri oluşturmak için

1. Normal olarak [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] bir uygulama oluşturun veya mevcut [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamanızı kullanın.

2. Uygulama bildirimini Not Defteri gibi bir metin veya XML düzenleyicisiyle açın.

3. `assembly` Öğesini bulun. Daha fazla bilgi için bkz. [ClickOnce uygulama bildirimi](../deployment/clickonce-application-manifest.md).

4. `assembly` Öğesinin bir alt öğesi olarak bir `fileAssociation` öğesi ekleyin. `fileAssociation` Öğesi dört özniteliğe sahiptir:

   - `extension`: Uygulamayla ilişkilendirmek istediğiniz dosya adı uzantısı.

   - `description`: Windows kabuğu 'nda görünecek dosya türünün açıklaması.

   - `progid`: Kayıt defterinde işaretlemek için dosya türünü benzersiz bir şekilde tanımlayan bir dize.

   - `defaultIcon`: Bu dosya türü için kullanılacak simge. Simgenin uygulama bildiriminde bir dosya kaynağı olarak eklenmesi gerekir. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulamasına](../deployment/how-to-include-a-data-file-in-a-clickonce-application.md)bir veri dosyası ekleyin.

     `file` Ve`fileAssociation` öğelerinin bir örneği için bkz [ \<. FileAssociation > öğesi](../deployment/fileassociation-element-clickonce-application.md).

5. Birden çok dosya türünü uygulamayla ilişkilendirmek istiyorsanız, ek `fileAssociation` öğeler ekleyin. `progid` Özniteliğin her biri için farklı olması gerektiğini unutmayın.

6. Uygulama bildirimini tamamladıktan sonra, bildirimi yeniden imzalayın. Bunu komut satırından *Mage. exe*' yi kullanarak yapabilirsiniz.

    `mage -Sign WindowsFormsApp1.exe.manifest -CertFile mycert.pfx`

    Daha fazla bilgi için bkz. [Mage. exe (bildirim oluşturma ve düzenleme aracı)](/dotnet/framework/tools/mage-exe-manifest-generation-and-editing-tool).

## <a name="see-also"></a>Ayrıca bkz.
- [\<fileAssociation > öğesi](../deployment/fileassociation-element-clickonce-application.md)
- [ClickOnce uygulama bildirimi](../deployment/clickonce-application-manifest.md)
- [Mage.exe (Bildirim Oluşturma ve Düzenleme Aracı)](/dotnet/framework/tools/mage-exe-manifest-generation-and-editing-tool)