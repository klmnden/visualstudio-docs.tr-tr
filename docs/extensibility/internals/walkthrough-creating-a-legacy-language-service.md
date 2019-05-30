---
title: 'İzlenecek yol: Eski dil hizmeti oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- language services [managed package framework], creating
ms.assetid: 6a5dd2c2-261b-4efd-a3f4-8fb90b73dc82
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1d5fdffa76f273bc8ff7b7bdf18ce9db99a9052e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323409"
---
# <a name="walkthrough-creating-a-legacy-language-service"></a>İzlenecek yol: Eski Dil Hizmeti oluşturma
Bir dil hizmeti uygulamak için yönetilen paket framework (MPF) dil sınıfları kullanarak [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] oldukça basittir. Dil hizmeti ve dil hizmeti diliniz için bir ayrıştırıcı barındırmak için bir VSPackage ihtiyacınız vardır.

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolda takip etmek için Visual Studio SDK'yı yüklemeniz gerekir. Daha fazla bilgi için [Visual Studio SDK](../../extensibility/visual-studio-sdk.md).

## <a name="locations-for-the-visual-studio-package-project-template"></a>Visual Studio Paket projesi şablonu için konumları
 Visual Studio Paket proje şablonu, üç farklı şablonu konumlarda bulunabilir **yeni proje** iletişim kutusunda:

1. Visual Basic genişletilebilirliği altında. Visual Basic proje varsayılan dildir.

2. C# genişletilebilirlik altında. Varsayılan proje C# dilidir.

3. Diğer proje türleri genişletilebilirliği altında. C++ projesinin varsayılan dildir.

### <a name="create-a-vspackage"></a>VSPackage'ı oluşturma

1. Visual Studio Paket proje şablonuyla yeni bir VSPackage'ı oluşturun.

    Dil hizmeti için mevcut bir VSPackage ekliyorsanız, aşağıdaki adımları atlayın ve doğrudan "dil hizmeti Sınıf Oluştur" yordamına gidin.

2. MyLanguagePackage projesinin adını girin ve tıklatın **Tamam**.

    İstediğiniz herhangi bir adı kullanabilirsiniz. Bu yordamlar burada ayrıntıları MyLanguagePackage adı olarak varsayılır.

3. Seçin [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] dil ve yeni bir anahtar dosyası oluştur seçeneği olarak. **İleri**'ye tıklayın.

4. Uygun şirket ve paket bilgileri girin. **İleri**'ye tıklayın.

5. Seçin **menü komutu**. **İleri**'ye tıklayın.

    Kod parçacıkları desteklemek düşünmüyorsanız, yalnızca Son'a tıklayın ve sonraki adıma yoksay.

6. Girin **kod parçacığı Ekle** olarak **komut adı** ve `cmdidInsertSnippet` için **komut kimliği**. **Son**'a tıklayın.

    **Komut adı** ve **komut kimliği** istediğiniz olabilir, bunlar yalnızca örnektir.

### <a name="create-the-language-service-class"></a>Dil hizmeti sınıfı oluşturma

1. İçinde **Çözüm Gezgini**, MyLanguagePackage projeye sağ tıklayın, seçin **Ekle**, **başvuru**ve ardından **Yeni Başvuru Ekle** düğmesi.

2. İçinde **Başvuru Ekle** iletişim kutusunda **Microsoft.VisualStudio.Package.LanguageService** içinde **.NET** sekmesine **Tamam**.

     Bu dil paketi projesi için yalnızca bir kez gerçekleştirilmesi gerekir.

3. İçinde **Çözüm Gezgini**VSPackage projeye sağ tıklayın ve seçin **Ekle**, **sınıfı**.

4. Emin **sınıfı** şablonları listesinde seçilir.

5. Girin **MyLanguageService.cs** tıklatın ve sınıf dosyası adını **Ekle**.

     İstediğiniz herhangi bir adı kullanabilirsiniz. Bu yordamlar burada ayrıntıları varsayar `MyLanguageService` adı.

6. MyLanguageService.cs dosyasına aşağıdakileri ekleyin `using` deyimleri.

     [!code-csharp[CreatingALanguageService(ManagedPackageFramework)#1](../../extensibility/internals/codesnippet/CSharp/walkthrough-creating-a-legacy-language-service_1.cs)]
     [!code-vb[CreatingALanguageService(ManagedPackageFramework)#1](../../extensibility/internals/codesnippet/VisualBasic/walkthrough-creating-a-legacy-language-service_1.vb)]

7. Değiştirme `MyLanguageService` öğesinden türetilen sınıfın <xref:Microsoft.VisualStudio.Package.LanguageService> sınıfı:

     [!code-csharp[CreatingALanguageService(ManagedPackageFramework)#2](../../extensibility/internals/codesnippet/CSharp/walkthrough-creating-a-legacy-language-service_2.cs)]
     [!code-vb[CreatingALanguageService(ManagedPackageFramework)#2](../../extensibility/internals/codesnippet/VisualBasic/walkthrough-creating-a-legacy-language-service_2.vb)]

8. Gelen ve "LanguageService" imleci konumlandırma **Düzenle**, **IntelliSense** menüsünde **soyut sınıf Uygula**. Bu, bir dil hizmeti sınıf uygulamak için en düşük gerekli yöntemleri ekler.

9. Soyut metotlar açıklandığı gibi uygulamak [eski dil hizmetinde uygulama](../../extensibility/internals/implementing-a-legacy-language-service2.md).

### <a name="register-the-language-service"></a>Dil hizmetine kaydetme

1. MyLanguagePackagePackage.cs dosyasını açın ve aşağıdakileri ekleyin `using` ifadeleri:

     [!code-vb[CreatingALanguageService(ManagedPackageFramework)#3](../../extensibility/internals/codesnippet/VisualBasic/walkthrough-creating-a-legacy-language-service_3.vb)]
     [!code-csharp[CreatingALanguageService(ManagedPackageFramework)#3](../../extensibility/internals/codesnippet/CSharp/walkthrough-creating-a-legacy-language-service_3.cs)]

2. Dil hizmeti sınıfınıza açıklandığı kaydetme [eski dil hizmetinde kaydetme](../../extensibility/internals/registering-a-legacy-language-service1.md). Bu, "Dil hizmeti Proffering" bölümleri ve ProvideXX öznitelikleri içerir. Burada bu konuda TestLanguageService kullanan MyLanguageService kullanın.

### <a name="the-parser-and-scanner"></a>Ayrıştırıcısı ve tarayıcısı

1. Bir ayrıştırıcısı ve tarayıcısı dil açıklandığı gibi uygulamak [eski dil hizmeti ayrıştırıcısı ve tarayıcısı](../../extensibility/internals/legacy-language-service-parser-and-scanner.md).

     Ayrıştırıcısı ve tarayıcısı nasıl uygulayacağınıza tamamen size bağlıdır ve bu konunun kapsamı dışındadır.

## <a name="language-service-features"></a>Dil hizmeti özellikleri
 Dil hizmetinde her özelliği uygulamak için genellikle uygun MPF dil hizmeti sınıfından bir sınıf türetin gerektiği gibi tüm soyut yöntemlerini uygular ve uygun yöntemleri geçersiz kılın. Desteklemek istiyorsanız, oluşturun ve/veya öğesinden türetilen sınıfları özelliklerine bağımlıdır. Bu özellikleri ayrıntılı olarak ele alınmıştır [eski dil hizmeti özellikleri](../../extensibility/internals/legacy-language-service-features1.md). Aşağıdaki yordam, bir sınıf MPF sınıflarından türetme için genel yaklaşım kullanılır.

#### <a name="deriving-from-an-mpf-class"></a>Bir MPF sınıftan türetme

1. İçinde **Çözüm Gezgini**VSPackage projeye sağ tıklayın ve seçin **Ekle**, **sınıfı**.

2. Emin **sınıfı** şablonları listesinde seçilir.

     Sınıf dosyası için uygun bir ad girin ve tıklayın **Ekle**.

3. Yeni sınıf dosyasında, aşağıdaki ekleyin `using` deyimleri.

     [!code-csharp[CreatingALanguageService(ManagedPackageFramework)#4](../../extensibility/internals/codesnippet/CSharp/walkthrough-creating-a-legacy-language-service_4.cs)]
     [!code-vb[CreatingALanguageService(ManagedPackageFramework)#4](../../extensibility/internals/codesnippet/VisualBasic/walkthrough-creating-a-legacy-language-service_4.vb)]

4. İstenen MPF sınıfından türetilir için sınıfı değiştirin.

5. En az temel sınıfın Oluşturucusu aynı parametreleri alan bir sınıf oluşturucu ekleyin ve Oluşturucusu parametreleri temel sınıf oluşturucusunu açın.

     Bir sınıf için oluşturucu gibi türetilen <xref:Microsoft.VisualStudio.Package.Source> sınıfı aşağıdaki gibi görünebilir:

     [!code-csharp[CreatingALanguageService(ManagedPackageFramework)#5](../../extensibility/internals/codesnippet/CSharp/walkthrough-creating-a-legacy-language-service_5.cs)]
     [!code-vb[CreatingALanguageService(ManagedPackageFramework)#5](../../extensibility/internals/codesnippet/VisualBasic/walkthrough-creating-a-legacy-language-service_5.vb)]

6. Gelen **Düzenle**, **IntelliSense** menüsünde **soyut sınıf Uygula** temel sınıfta uygulanması gereken tüm soyut yöntemler varsa.

7. Aksi takdirde, giriş işaretini sınıf içinde getirin ve geçersiz kılınacak yöntemi girin.

     Örneğin `public override` bu sınıfta geçersiz kılınabilir tüm yöntemlerin listesini görmek için.

## <a name="see-also"></a>Ayrıca Bkz.
- [Eski Dil Hizmeti Uygulama](../../extensibility/internals/implementing-a-legacy-language-service1.md)