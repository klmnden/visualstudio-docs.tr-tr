---
title: 'Nasıl yapılır: Oluşturun. Vsct dosyası | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, creating
ms.assetid: b955f51c-f9f9-49c3-a8e4-63b6eb0e0341
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c3155ff69db461e652b11ff6e8ec6d405000244f
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68924180"
---
# <a name="how-to-create-a-vsct-file"></a>Nasıl yapılır: . Vsct dosyası oluşturma

XML tabanlı Visual Studio komut tablosu yapılandırma ( *. vsct*) dosyası oluşturmanın birkaç yolu vardır.

- [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Paket şablonunda yeni bir VSPackage oluşturabilirsiniz.

- Var olan bir *. CTC* dosyasından bir dosya oluşturmak için XML tabanlı komut tablosu yapılandırma derleyicisi olan *vsct. exe*' yi kullanabilirsiniz.

- Varolan bir *. CTO* dosyasından bir *. vsct* dosyası oluşturmak için *vsct. exe* ' yi kullanabilirsiniz.

- El ile yeni bir *. vsct* dosyası oluşturabilirsiniz.

  Bu makalede, el ile yeni bir *. vsct* dosyası oluşturma açıklanır.

### <a name="to-manually-create-a-new-vsct-file"></a>El ile yeni bir. vsct dosyası oluşturmak için

1. Başlangıç [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

2. Üzerinde **dosya** menüsünde **yeni**ve ardından **dosya**.

3. **Şablonlar** bölmesinde, **XML dosyası** ' na ve sonra **Aç**' a tıklayın.

4. **Görünüm** menüsünde **Özellikler** ' e tıklayarak XML dosyasının özelliklerini görüntüleyin.

5. **Özellikler** penceresinde, **şemalar** özelliğindeki **Gözden** geçirme düğmesine tıklayın.

6. XSD şemaları listesinde *vsct. xsd* şemasını seçin. Listede yoksa, **Ekle** ' ye tıklayın ve dosyayı yerel bir sürücüde bulun. İşiniz bittiğinde **Tamam** ' a tıklayın.

7. XML dosyasında *< CommandTable* yazın ve ardından **Tab**tuşuna basın. Yazarak *>* etiketi kapatın.

    Bu eylem, temel bir *. vsct* dosyası oluşturur.

8. [VSCT XML şema başvurusuna](../../extensibility/vsct-xml-schema-reference.md)göre eklemek istediğiniz XML dosyasının öğelerini girin. Daha fazla bilgi için bkz. [Author. vsct dosyaları](../../extensibility/internals/authoring-dot-vsct-files.md).

<a name="how-to-create-a-dot-vsct-file-from-an-existing-dot-ctc-file"></a>

## <a name="how-to-create-a-vsct-file-from-an-existing-ctc-file"></a>Nasıl yapılır: Var olan bir. CTC dosyasından bir. vsct dosyası oluşturma

Varolan bir komut tablosu *. CTC* kaynak dosyasından XML tabanlı *. vsct* dosyası oluşturabilirsiniz. Bunu yaparak, yeni XML tabanlı [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] komut tablosu (vsct) derleyici biçiminden yararlanabilirsiniz.

### <a name="to-create-a-vsct-file-from-a-ctc-file"></a>. CTC dosyasından bir. vsct dosyası oluşturmak için

1. Perl dilinin bir kopyasını alın.

2. *Genellikle \<Visual Studio SDK yükleme yolu > \VisualStudioIntegration\Tools\bin* klasöründe bulunan Perl betiği *ConvertCTCToVSCT.pl*bir kopyasını edinin.

3. Dönüştürmek istediğiniz *. CTC* kaynak dosyasının bir kopyasını alın.

4. Dosyaları aynı dizine yerleştirin.

5. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Komut istemi penceresinde, dizinine gidin.

6. Tür

   ```
   perl.exe ConvertCTCtoVSCT.pl PkgCmd.ctc PkgCmd.vsct
   ```

    Burada *PkgCmd. CTC* , *. CTC* dosyasının adı ve *PkgCmd. vsct* , oluşturmak istediğiniz *. vsct* dosyasının adıdır.

    Bu eylem yeni bir *. vsct* XML komut tablosu kaynak dosyası oluşturur. Vsct *. exe*, vsct derleyicisini kullanarak dosyayı herhangi bir *. vsct* dosyası gibi derleyebilirsiniz.

   > [!NOTE]
   > XML açıklamalarını yeniden düzenleyerek *. vsct* dosyasının okunabilirliğini geliştirebilirsiniz.

<a name="how-to-create-a-dot-vsct-file-from-an-existing-dot-cto-file"></a>

## <a name="how-to-create-a-vsct-file-from-an-existing-cto-file"></a>Nasıl yapılır: Var olan bir. CTO dosyasından bir. vsct dosyası oluşturma

Var olan bir binary *. CTO* dosyasından XML tabanlı *. vsct* dosyası oluşturabilirsiniz. Bunun yapılması, yeni komut tablosu derleyici biçiminden yararlanmanızı sağlar. *. CTO* dosyası bir *. CTC* dosyasından derlense bile bu işlem işe yarar. *. Vsct* dosyasını başka bir. cto dosyasına düzenleyebilir ve derleyebilirsiniz.

### <a name="to-create-a-vsct-file-from-a-cto-file"></a>. CTO dosyasından bir. vsct dosyası oluşturmak için

1. *. CTO* dosyasının ve karşılık gelen *. ctsyma* dosyasının kopyalarını alın.

2. Dosyaları *vsct. exe* derleyicisi ile aynı dizine yerleştirin.

3. Visual Studio komut isteminde *. CTO* ve *. ctsyd* dosyalarını içeren dizine gidin.

4. Tür

    ```
    vsct.exe <ctofilename>.cto <vsctfilename>.vsct -S<symfilename>.ctsym
    ```

     Burada \<ctofilename\> *. CTO* dosyasının adıdır, vsctfilename \<\> , oluşturmak istediğiniz *. vsct* dosyasının adıdır ve \<symfilename\> , *. ctsyd* dosyası.

     Bu işlem yeni bir *. vsct* XML komut tablosu derleyici dosyası oluşturur. Dosyayı herhangi bir *. vsct* dosyası gibi *vsct. exe*, vsct derleyicisi ile düzenleyebilir ve derleyebilirsiniz.

## <a name="compile-the-code"></a>Kod derleme
 Yalnızca bir *. vsct* dosyasını bir projeye eklemek, derlemeye neden olmaz. Yapı sürecinde bu dosyayı eklemeniz gerekir.

### <a name="to-add-a-vsct-file-to-project-compilation"></a>Proje derlemesine bir. vsct dosyası eklemek için

1. Proje dosyanızı düzenleyicide açın. Proje yüklüyse, önce onu kaldırmanız gerekir.

2. Aşağıdaki örnekte gösterildiği gibi, bir `VSCTCompile` öğesi içeren bir [ItemGroup öğesi](../../msbuild/itemgroup-element-msbuild.md) ekleyin.

    ```xml
    <ItemGroup>
      <VSCTCompile Include="TopLevelMenu.vsct">
        <ResourceName>Menus.ctmenu</ResourceName>
      </VSCTCompile>
    </ItemGroup>

    ```

     Öğesi her zaman olarak `Menus.ctmenu`ayarlanmalıdır. `ResourceName`

3. Projeniz bir *. resx* dosyası içeriyorsa, aşağıdaki örnekte gösterildiği gibi `EmbeddedResource` bir `MergeWithCTO` öğesi içeren bir öğesi ekleyin:

    ```xml
    <EmbeddedResource Include="VSPackage.resx">
      <MergeWithCTO>true</MergeWithCTO>
      <ManifestResourceName>VSPackage</ManifestResourceName>
    </EmbeddedResource>

    ```

     Bu biçimlendirme, `ItemGroup` gömülü kaynakları içeren öğenin içinde olmalıdır.

4. Genellikle, düzenleyicide  *\<ProjectName\>Package.cs* veya  *\<ProjectNamePackage.vbadlıpaketdosyasınıaçın.\>*

5. Aşağıdaki örnekte `ProvideMenuResource` gösterildiği gibi, Package sınıfına bir öznitelik ekleyin.

    ```csharp
    [ProvideMenuResource("Menus.ctmenu", 1)]
    ```

     İlk parametre değeri proje dosyasında tanımladığınız `ResourceName` özniteliğin değeriyle eşleşmelidir.

## <a name="see-also"></a>Ayrıca bkz.
- [Author. vsct dosyaları](../../extensibility/internals/authoring-dot-vsct-files.md)
- [Visual Studio komut tablosu (. vsct) dosyaları](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
- [VSCT XML Şeması Başvurusu](../../extensibility/vsct-xml-schema-reference.md)