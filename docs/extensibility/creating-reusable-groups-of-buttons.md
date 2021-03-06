---
title: Yeniden kullanılabilir düğme grupları oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- button groups, creating in VSPackages
- VSPackages, creating reusable button groups
- buttons, creating reusable groups
ms.assetid: 0c561617-fb86-476d-8bd1-c6e5e7464c65
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 454e42ba0b99d47048fa54527e8771f8294dcbc9
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351986"
---
# <a name="create-reusable-groups-of-buttons"></a>Yeniden kullanılabilir düğme grupları oluşturma
Bir komut grubuyla, her zaman birlikte bir menü veya araç çubuğunda görünen komutlar koleksiyonudur. Herhangi bir komut grubu CommandPlacements bölümündeki farklı üst menüye atayarak yeniden kullanılabilir *.vsct* dosya.

 Komut grupları genellikle düğmeleri içerir, ancak bunlar diğer menü veya birleşik giriş kutuları de içerebilir.

## <a name="to-create-a-reusable-group-of-buttons"></a>Düğme yeniden kullanılabilir bir grup oluşturmak için

1. Adlı bir VSIX projesi oluşturun `ReusableButtons`. Daha fazla bilgi için [bir menü komutuyla uzantı oluşturma](../extensibility/creating-an-extension-with-a-menu-command.md).

2. Projeyi açtığında, adlı bir özel komut öğesi şablonu ekleme **ReusableCommand**. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Ekle** > **yeni öğe**. İçinde **Yeni Öğe Ekle** iletişim kutusunda, Git **Visual C#**  > **genişletilebilirlik** seçip **özel komut**. İçinde **adı** alan penceresinin en altında komut dosyası adı için değiştirme *ReusableCommand.cs*.

3. İçinde *.vsct* dosya, semboller bölümüne gidin ve grupları ve proje için komutları içeren GuidSymbol öğesi bulunamadı. GuidReusableCommandPackageCmdSet adlandırılmalıdır.

4. Aşağıdaki örnekte olduğu gibi gruba eklediğiniz her düğme için bir Idsymbol ekleyin.

    ```xml
    <GuidSymbol name="guidReusableCommandPackageCmdSet" value="{7f383b2a-c6b9-4c1d-b4b8-a26dc5b60ca1}">
        <IDSymbol name="MyMenuGroup" value="0x1020" />
        <IDSymbol name="ReusableCommandId" value="0x0100" />
        <IDSymbol name="SecondReusableCommandId" value="0x0200" />
    </GuidSymbol>
    ```

     Varsayılan olarak, komut öğe şablonu adlı bir grup oluşturur. **MyMenuGroup** ve her bir Idsymbol giriş ile birlikte sağlanan ada sahip bir düğme.

5. Grupları bölümünde sembolleri bölümde verilen olanlarla aynı GUID ve ID özniteliklere sahip bir Grup öğesi oluşturun. Ayrıca, mevcut bir grubunu kullanın veya aşağıdaki örnekteki gibi komut şablonu tarafından sağlanan giriş kullanabilirsiniz. Bu grubun görünen **Araçları** menüsü

    ```xml
    <Groups>
        <Group guid="guidReusableCommandPackageCmdSet" id="MyMenuGroup" priority="0x0600">
              <Parent guid="guidSHLMainMenu" id="IDM_VS_MENU_TOOLS"/>
        </Group>
    </Groups>
    ```

## <a name="to-create-a-group-of-buttons-for-reuse"></a>Düğme yeniden kullanım için bir grup oluşturmak için

1. Menü ve komut tanımı içinde üst olarak kullanarak veya koyarak komutu veya menü grubunda CommandPlacements bölümünü kullanarak, bir gruptaki bir komut veya menüyü koyabilirsiniz.

     Düğmeler bölümünde grubunuz üst öğe olarak bulunan bir düğme tanımlayın veya aşağıdaki örnekte gösterildiği gibi paket şablon tarafından sağlanan düğmesini kullanın.

    ```xml
    <Button guid="guidReusableCommandPackageCmdSet" id="ReusableCommandId" priority="0x0100" type="Button">
        <Parent guid="guidReusableCommandPackageCmdSet" id="MyMenuGroup" />
        <Icon guid="guidImages" id="bmpPic1" />
        <Strings>
            <ButtonText>Invoke ReusableCommand</ButtonText>
        </Strings>
    </Button>
    ```

2. Bir düğmeyi birden fazla grubunda bulunmasını istiyorsanız, bir giriş için komutları bölümünden sonra yerleştirilmelidir CommandPlacements bölümdeki oluşturun. Yerleştirmek istediğiniz düğmenin uyacak şekilde CommandPlacement öğesi GUID ve ID özniteliklerini ayarlayın ve ardından GUID ve ID öğesi üst öğesi bu hedef grubun aşağıdaki örnekte gösterilen şekilde ayarlayın.

    ```xml
    <CommandPlacements>
        <CommandPlacement guid="guidReusableCommandPackageCmdSet" id="SecondReusableCommandId" priority="0x105">
          <Parent guid="guidReusableCommandPackageCmdSet" id="MyMenuGroup" />
        </CommandPlacement>
    </CommandPlacements>
    ```

    > [!NOTE]
    > Önceliği alanının değeri, yeni komut grubu komutu konumunu belirler. Öğe öğe tanımında ayarlanan geçersiz kılar CommandPlacement öncelikler ayarlayın. Düşük öncelikli değerlere sahip komutları önce daha yüksek öncelik değerine sahip komutlar görüntülenir. Yinelenen öncelik değerleri izin verilir, ancak aynı öncelik değerine sahip komutları göreli konumunu, çünkü garanti edilemez sırayı **devenv/Setup** komut, kayıt defterinden son arabirimi oluşturur tutarlı olmayabilir.

## <a name="to-put-a-reusable-group-of-buttons-on-a-menu"></a>Düğmeleri yeniden kullanılabilir bir grup bir menüye yerleştirmek için

1. Girdi oluşturma `CommandPlacements` bölümü. GUID ve Kimliğini `CommandPlacement` grubunuzun, bu öğeye üst GUID ve ID bu hedef konumu ayarlayın.

    CommandPlacements bölümü komutları Kısım sonra yerleştirilmelidir:

   ```xml
   <CommandTable>
   ...
     <Commands>... </Commands>
     <CommandPlacements>... </CommandPlacements>
   ...
   </CommandTable>
   ```

    Bir komut grubuyla birden fazla menüsünde eklenebilir. Üst menü, oluşturduğunuz tarafından sağlanan bir olabilir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] (açıklandığı *ShellCmdDef.vsct* veya *SharedCmdDef.vsct*), ya da başka bir VSPackage içinde tanımlanır. Üst menü sonunda bağlı olduğu sürece, ana öğe katmanları sayısı sınırsızdır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] veya VSPackage tarafından görüntülenen bir kısayol menüsü.

    Aşağıdaki örnek grubu koyar **Çözüm Gezgini** diğer düğmeleri sağındaki araç çubuğu.

   ```xml
   <CommandPlacements>
       <CommandPlacement guid="guidReusableCommandPackageCmdSet" id="MyMenuGroup" priority="0xF00">
         <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_PROJWIN"/>
       </CommandPlacement>
   </CommandPlacements>
   ```

   ```xml
   <CommandPlacements>
     <CommandPlacement guid="guidButtonGroupCmdSet" id="MyMenuGroup"
         priority="0x605">
       <Parent guid="guidSHLMainMenu" id="IDM_VS_MENU_TOOLS" />
     </CommandPlacement>
   </CommandPlacements>

   ```
