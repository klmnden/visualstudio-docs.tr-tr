---
title: 'İzlenecek yol: C/C++ Kodunda Hata Olup Olmadığını Analiz Etme'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- C/C++, code analysis
- code analysis, walkthroughs
- code, analyzing C/C++
- code analysis tool, walkthroughs
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- cplusplus
ms.openlocfilehash: acfa1e274b7c0744c2d9968682960b1cd50e0044
ms.sourcegitcommit: 2dc924c96a6d48803c8eedc3d6781202629b41fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57736933"
---
# <a name="walkthrough-analyzing-cc-code-for-defects"></a>İzlenecek yol: C/C++ Kodunda Hata Olup Olmadığını Analiz Etme

Bu yönerge, C/C++ kodu için kod analizi aracı kullanarak olası kod kusurları için C/C++ kodunu analiz etme gösterir.

- Yerel kod üzerinde kod analizini Çalıştır.
- Kod hatasını uyarıları çözümleyin.
- Hata olarak kabul uyarısı.
- Kod hata analizi iyileştirmek için kaynak kodu açıklama ekleyin.

## <a name="prerequisites"></a>Önkoşullar

- Bir kopyasını [gösterim örneği](../code-quality/demo-sample.md).
- C/C++ temel düzeyde bilinmesini.

### <a name="to-run-code-defect-analysis-on-native-code"></a>Yerel kod üzerinde kod hata analizi çalıştırmak için

1. Tanıtım çözümde açık [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].

     Tanıtım çözümü şimdi doldurur **Çözüm Gezgini**.

2. Üzerinde **derleme** menüsünde tıklatın **çözümü yeniden derle**.

     Çözüm herhangi bir hata veya uyarı derlenir.

3. İçinde **Çözüm Gezgini**, CodeDefects projeyi seçin.

4. Üzerinde **proje** menüsünü tıklatın **özellikleri**.

     **CodeDefects özellik sayfaları** iletişim kutusu görüntülenir.

5. Tıklayın **Kod Analizi**.

6. Tıklayın **C/c++ derlemede kod çözümlemeyi etkinleştir** onay kutusu.

7. CodeDefects projeyi yeniden derleyin.

     Kod çözümleme uyarıları görüntülenir **hata listesi**.

### <a name="to-analyze-code-defect-warnings"></a>Kod hatasını uyarıları çözümlemek için

1. Üzerinde **görünümü** menüsünü tıklatın **hata listesi**.

     Te seçtiğiniz Geliştirici profili bağlı olarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], işaret edecek şekilde olabilir **diğer Windows** üzerinde **görünümü** menüsüne ve ardından **hata listesi**.

2. İçinde **hata listesi**, aşağıdaki uyarıyı çift tıklatın:

     Uyarı C6230: Anlamsal olarak farklı türleri arasında örtük atama: Boole bağlamında HRESULT kullanma.

     Kod Düzenleyicisi uyarıya yol açan işlev satır görüntüler `bool ProcessDomain()`. Bu uyarı, bir HRESULT bir 'If' deyimi bir Boolean sonucu beklenen yeri kullanılmakta olduğunu gösterir.

3. Bu uyarı, SUCCEEDED makrosu kullanarak düzeltin. Kodunuzu aşağıdaki koda benzemelidir:

   ```cpp
   if (SUCCEEDED (ReadUserAccount()) )
   ```

4. İçinde **hata listesi**, aşağıdaki uyarıyı çift tıklatın:

     C6282 Uyarı: Hatalı operatör: test bağlamında sabit atama. Hedeflenen == oldu?

5. Bu uyarı, eşitlik için test ederek düzeltin. Kodunuzu aşağıdaki koda benzemelidir:

   ```cpp
   if ((len == ACCOUNT_DOMAIN_LEN) || (g_userAccount[len] != '\\'))
   ```

### <a name="to-treat-warning-as-an-error"></a>Uyarı hata olarak değerlendirilecek

1. Bug.cpp dosyasına aşağıdakileri ekleyin `#pragma` C6001 uyarı hata olarak değerlendirilecek dosyanın başına deyimi:

   ```cpp
   #pragma warning (error: 6001)
   ```

2. CodeDefects projeyi yeniden derleyin.

     İçinde **hata listesi**, C6001 hata olarak görünür.

3. Kalan iki C6001 hataları düzeltin **hata listesi** başlatma tarafından `i` ve `j` 0.

4. CodeDefects projeyi yeniden derleyin.

     Projeyi herhangi bir uyarı veya hata derler.

### <a name="to-correct-the-source-code-annotation-warnings-in-annotationc"></a>Kaynak kod ek açıklama uyarılara annotation.c düzeltmek için

1. Çözüm Gezgini içinde ek açıklamalar projeyi seçin.

2. Üzerinde **proje** menüsünü tıklatın **özellikleri**.

     **Ek açıklamaları özellik sayfaları** iletişim kutusu görüntülenir.

3. Tıklayın **Kod Analizi**.

4. Seçin **C/c++ derlemede kod çözümlemeyi etkinleştir** onay kutusu.

5. Ek açıklamalar projeyi yeniden derleyin.

6. İçinde **hata listesi**, aşağıdaki uyarıyı çift tıklatın:

     Uyarı C6011: NULL işaretçi 'newNode' başvurusunun kaldırılması.

     Bu uyarı, dönüş değeri denetleyin çağıran tarafından hatası gösterir. Bu durumda, bir çağrıda **AllocateNode** NULL bir değer döndürebilir (işlev bildirimi için AllocateNode annotations.h üstbilgi dosyasını bakın).

7. Annotations.cpp dosyasını açın.

8. Bu uyarıyı düzeltmek için dönüş değerini test etmek için bir 'if' deyimini kullanın. Kodunuzu aşağıdaki koda benzemelidir:

   ```cpp
   if (NULL != newNode)
   {
   newNode->data = value;
   newNode->next = 0;
   node->next = newNode;
   }
   ```

9. Ek açıklamalar projeyi yeniden derleyin.

     Projeyi herhangi bir uyarı veya hata derler.

### <a name="to-use-source-code-annotation"></a>Kaynak kod ek açıklamaları kullanmak için

1. Ek açıklama biçimsel parametreler ve dönüş değeri işlevin `AddTail` öncesi ve sonrası koşulları Bu örnekte gösterilen şekilde kullanarak:

   ```cpp
   [returnvalue:SA_Post (Null=SA_Maybe)] LinkedList* AddTail
   (
   [SA_Pre(Null=SA_Maybe)] LinkedList* node,
   int value
   )
   ```

2. Ek açıklamalar projeyi yeniden derleyin.

3. İçinde **hata listesi**, aşağıdaki uyarıyı çift tıklatın:

     Uyarı C6011: 'Düğümü' NULL işaretçisinin başvurusunun kaldırılması.

     Bu uyarı işleve geçirilen düğüm null olabileceğini gösterir ve burada uyarı tetiklendi satır numarasını gösterir.

4. Bu uyarıyı düzeltmek için dönüş değerini test etmek için bir 'if' deyimini kullanın. Kodunuzu aşağıdaki koda benzemelidir:

   ```cpp
   . . .
   LinkedList *newNode = NULL;
   if (NULL == node)
   {
        return NULL;
        . . .
   }
   ```

5. Ek açıklamalar projeyi yeniden derleyin.

     Projeyi herhangi bir uyarı veya hata derler.

## <a name="see-also"></a>Ayrıca bkz.

[İzlenecek yol: Kod kusurları için yönetilen kodu analiz etme](../code-quality/walkthrough-analyzing-managed-code-for-code-defects.md)
[C/C++ için Kod Analizi](../code-quality/code-analysis-for-c-cpp-overview.md)
