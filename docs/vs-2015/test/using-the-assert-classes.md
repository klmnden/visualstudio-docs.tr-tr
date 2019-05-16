---
title: Onay sınıfları kullanma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
helpviewer_keywords:
- Assert classes
- Assert statements
- unit tests, Assert statements
- unit tests, Assert classes
ms.assetid: da1b7a0d-4f1d-4d50-a07e-7b3ff60053f9
caps.latest.revision: 29
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: fc27b7b0c0e277a0e39b406a07d677fe25bf8e73
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65695073"
---
# <a name="using-the-assert-classes"></a>Onay Sınıfları Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Onay sınıfları UnitTestingFramework ad alanı, belirli işlevselliğini doğrulamak için kullanın. Kod geliştirme kodunuzda bir yöntemin bir birim sınaması metodunda uygular, ancak yalnızca Assert deyimleri eklerseniz kodun davranışı doğruluğunu rapor.  
  
## <a name="kinds-of-asserts"></a>Tür, onaylar  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting> Onay sınıfları çeşitli ad alanı sağlar:  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert>  
  
 Test yönteminizde herhangi bir sayıda Assert.AreEqual() gibi onay sınıfının yöntemlerini çağırabilirsiniz. Assert sınıfın aralarından seçim yapabileceğiniz birçok yöntem vardır ve bu yöntemlerin çoğunun çeşitli aşırı yükler vardır.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.CollectionAssert>  
  
 CollectionAssert sınıfı nesne koleksiyonları Karşılaştırılacak ve bir veya daha fazla koleksiyon durumunu doğrulamak için kullanın.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert>  
  
 StringAssert sınıfı, dizeleri karşılaştırmak için kullanın. Bu sınıf, çeşitli StringAssert.Contains StringAssert.Matches ve StringAssert.StartsWith gibi kullanışlı yöntemler içerir.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertFailedException>  
  
 Bir test başarısız olduğunda AssertFailedException özel durum oluşturulur. Zaman aşımına, beklenmeyen bir özel durum oluşturur veya başarısız sonucunu üreten bir onay deyimi içeren bir test başarısız olur.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertInconclusiveException>  
  
 Her bir test, yetersiz bir sonuç üretir assertınconclusiveexception oluşturur oluşturulur. Genellikle, hala henüz çalıştırılmaya hazır değil belirtmek için çalışmakta olduğunuz bir test için Assert.Inconclusive deyimi ekleyin.  
  
> [!NOTE]
> Ignore özniteliği ile çalıştırmaya hazır değil bir test işaretlemek için alternatif bir strateji olacaktır. Ancak, bu kolayca uygulamak için sol testlerin sayısı bir rapor oluşturulamıyor dezavantajı vardır.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.UnitTestAssertException>  
  
 Yeni bir onay özel durum sınıfı yazarsanız UnitTestAssertException taban sınıftan devralın o sınıfa sahip özel durum bir onaylama işlemi hatası yerine test veya üretim kodundan beklenmeyen bir özel durum olarak tanımlamak kolaylaştırır.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.ExpectedExceptionAttribute>  
  
 Geliştirme kodunuzdaki bir yöntemi tarafından oluşturulan beklediğiniz aslında bu yönteme durum olduğunu doğrulamak için test yönteminin istediğinizde ExpectedExceptionAttribute özniteliğine sahip bir test yöntemi süslemek.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting>   
 [Oluşturma ve varolan kod için birim testleri çalıştırma](https://msdn.microsoft.com/e8370b93-085b-41c9-8dec-655bd886f173)
