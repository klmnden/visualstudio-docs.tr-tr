---
title: '&lt;Dependency&gt; öğesi (ClickOnce uygulaması) | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#osVersionInfo
- urn:schemas-microsoft-com:asm.v2#os
- http://www.w3.org/2000/09/xmldsig#Transform
- urn:schemas-microsoft-com:asm.v2#dependency
- http://www.w3.org/2000/09/xmldsig#DigestValue
- urn:schemas-microsoft-com:asm.v2#assemblyIdentity
- http://www.w3.org/2000/09/xmldsig#DigestMethod
- http://www.w3.org/2000/09/xmldsig#Transforms
- urn:schemas-microsoft-com:asm.v2#hash
- urn:schemas-microsoft-com:asm.v2#dependentAssembly
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- manifests [ClickOnce], dependency element
- <dependency> element [ClickOnce application manifest]
ms.assetid: 09d6a1e0-60f8-4fbd-843b-8e49ee3115a3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3aa949aa2f8e718ab0209c54a0ea2160c042a4eb
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252490"
---
# <a name="ltdependencygt-element-clickonce-application"></a>&lt;Dependency&gt; öğesi (ClickOnce uygulaması)
Uygulama için gerekli olan platformu veya derleme bağımlılığını tanımlar.

## <a name="syntax"></a>Sözdizimi

```xml

      <dependency>
   <dependentOS
      supportURL
      description
   >
      <osVersionInfo>
         <os
            majorVersion
            minorVersion
            buildNumber
            servicePackMajor
            servicePackMinor
            productType
            suiteType
         />
      </osVersionInfo>
   </dependentOS>
   <dependentAssembly
      dependencyType
      allowDelayedBinding
      group
      codeBase
      size
   >
      <assemblyIdentity
         name
         version
         processorArchitecture
         language
      >
         <hash>
            <dsig:Transforms>
               <dsig:Transform
                  Algorithm
            />
            </dsig:Transforms>
            <dsig:DigestMethod />
            <dsig:DigestValue>
            </dsig:DigestValue>
    </hash>

      </assemblyIdentity>
   </dependentAssembly>
</dependency>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 `dependency` Öğe gereklidir. Aynı uygulama bildiriminde birden çok örneği `dependency` olabilir.

 `dependency` Öğesi özniteliklere sahip değildir ve aşağıdaki alt öğeleri içerir.

### <a name="dependentos"></a>Bağımlılık TOS
 İsteğe bağlı. `osVersionInfo` Öğesini içerir. Ve öğeleri birbirini dışlıyor: bir veya diğeri bir `dependency` öğe için bulunmalıdır, ancak her ikisine birden değil. `dependentAssembly` `dependentOS`

 `dependentOS`Aşağıdaki öznitelikleri destekler.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`supportUrl`|İsteğe bağlı. Bağımlı platform için bir destek URL 'SI belirtir. Gerekli platform bulunursa, bu URL kullanıcıya gösterilir.|
|`description`|İsteğe bağlı. `dependentOS` Öğesi tarafından tanımlanan işletim sistemini, insan tarafından okunabilen biçimde açıklar.|

### <a name="osversioninfo"></a>osVersionInfo
 Gerekli. Bu öğe, `dependentOS` öğesinin bir alt öğesidir ve `os` öğesi içerir. Bu öğenin öznitelikleri yok.

### <a name="os"></a>atayamadı
 Gerekli. Bu öğe, `osVersionInfo` öğesinin bir alt öğesidir. Bu öğe aşağıdaki özniteliklere sahiptir.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`majorVersion`|Gerekli. İşletim sisteminin ana sürüm numarasını belirtir.|
|`minorVersion`|Gerekli. İşletim sisteminin ikincil sürüm numarasını belirtir.|
|`buildNumber`|Gerekli. İşletim sisteminin yapı numarasını belirtir.|
|`servicePackMajor`|Gerekli. İşletim sisteminin hizmet paketi ana numarasını belirtir.|
|`servicePackMinor`|İsteğe bağlı. İşletim sisteminin hizmet paketi ikincil numarasını belirtir.|
|`productType`|İsteğe bağlı. Ürün türü değerini tanımlar. Geçerli değerler `server`, `workstation`, ve `domainController`. Örneğin, Windows 2000 Professional için bu öznitelik değeri ' dir `workstation`.|
|`suiteType`|İsteğe bağlı. Sistemde veya sistemin yapılandırma türünde bulunan bir ürün paketini tanımlar. Geçerli değerler şunlardır `backoffice` `blade` `datacenter` ,,`terminal`,,,,, ve. `enterprise` `home` `professional` `smallbusiness` `smallbusinessRestricted` Örneğin, Windows 2000 Professional için bu öznitelik değeri ' dir `professional`.|

### <a name="dependentassembly"></a>dependentAssembly
 İsteğe bağlı. `assemblyIdentity` Öğesini içerir. Ve öğeleri birbirini dışlıyor: bir veya diğeri bir `dependency` öğe için bulunmalıdır, ancak her ikisine birden değil. `dependentAssembly` `dependentOS`

 `dependentAssembly`Aşağıdaki özniteliklere sahiptir.

| Öznitelik | Açıklama |
|-----------------------| - |
| `dependencyType` | Gerekli. Bağımlılık türünü belirtir. Geçerli değerler ve `preprequisite` ' `install`dir. Derleme `install` ,[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamanın bir parçası olarak yüklenir. Uygulamanın `prerequisite` yüklenebilmesi için [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] önce bir derlemenin genel derleme önbelleğinde (GAC) mevcut olması gerekir. |
| `allowDelayedBinding` | Gerekli. Derlemenin çalışma zamanında programlı bir şekilde yüklenip yüklenemeyeceğini belirtir. |
| `group` | İsteğe bağlı. `dependencyType` Özniteliği olarak`install`ayarlandıysa, yalnızca istek üzerine yüklenen bir adlandırılmış derleme grubunu belirtir. Daha fazla bilgi için bkz [. İzlenecek yol: Tasarımcıyı](../deployment/walkthrough-downloading-assemblies-on-demand-with-the-clickonce-deployment-api-using-the-designer.md)kullanarak ClickOnce dağıtım API 'si Ile isteğe bağlı derlemeleri indirme.<br /><br /> Olarak `framework` ayarlıysa `prerequisite`ve özniteliği olarak ayarlanırsa, derlemeyi .NET Framework bir parçası olarak belirler. `dependencyType` Bu derleme için genel assemby Cache (GAC), .NET Framework 4 ve sonraki sürümlere yüklenirken denetlenmez. |
| `codeBase` | `dependencyType` Özniteliği olarak`install`ayarlandığında gereklidir. Bağımlı derlemenin yolu. Mutlak bir yol veya bildirimin kod tabanına göreli bir yol olabilir. Bu yol, Derleme bildiriminin geçerli olması için geçerli bir URI olmalıdır. |
| `size` | `dependencyType` Özniteliği olarak`install`ayarlandığında gereklidir. Bağımlı derlemenin bayt cinsinden boyutu. |

### <a name="assemblyidentity"></a>AssemblyIdentity
 Gerekli. Bu öğe, `dependentAssembly` öğesinin bir alt öğesidir ve aşağıdaki özniteliklere sahiptir.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`name`|Gerekli. Uygulamanın adını tanımlar.|
|`version`|Gerekli. Uygulamanın sürüm numarasını aşağıdaki biçimde belirtir:`major.minor.build.revision`|
|`publicKeyToken`|İsteğe bağlı. Uygulamanın veya derlemenin imzalandığı ortak anahtarın `SHA-1` karma değerinin son 8 baytını temsil eden 16 karakterlik bir onaltılık dize belirtir. Kataloğu imzalamak için kullanılan ortak anahtar 2048 bit veya daha fazla olmalıdır.|
|`processorArchitecture`|İsteğe bağlı. İşlemciyi belirtir. Geçerli değerler `x86` 32 bitlik Windows ve `I64` 64 bit Windows içindir.|
|`language`|İsteğe bağlı. Derlemenin EN-US gibi iki bölüm dil kodunu tanımlar.|

### <a name="hash"></a>hash
 Öğesi, `assemblyIdentity` öğesinin isteğe bağlı bir alt öğesidir. `hash` `hash` Öğesinde hiç öznitelik yok.

 [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]herhangi bir dosyanın dağıtımdan sonra değişmediğinden emin olmak için, bir uygulamadaki tüm dosyaların bir güvenlik denetimi olarak algoritmik karmasını kullanır. `hash` Öğe dahil değilse, bu denetim gerçekleştirilmez. Bu nedenle, `hash` öğesinin atlanması önerilmez.

### <a name="dsigtransforms"></a>dsig: dönüşümler
 Öğesi, `hash` öğesinin gerekli bir alt öğesidir. `dsig:Transforms` `dsig:Transforms` Öğesinde hiç öznitelik yok.

### <a name="dsigtransform"></a>dsig: dönüştürme
 Öğesi, `dsig:Transforms` öğesinin gerekli bir alt öğesidir. `dsig:Transform` `dsig:Transform` Öğesi aşağıdaki özniteliklere sahiptir.

| Öznitelik | Açıklama |
|-------------| - |
| `Algorithm` | Bu dosya için Özeti hesaplamak için kullanılan algoritma. Şu anda tarafından [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] `urn:schemas-microsoft-com:HashTransforms.Identity`kullanılan tek değer. |

### <a name="dsigdigestmethod"></a>dsig: DigestMethod
 Öğesi, `hash` öğesinin gerekli bir alt öğesidir. `dsig:DigestMethod` `dsig:DigestMethod` Öğesi aşağıdaki özniteliklere sahiptir.

| Öznitelik | Açıklama |
|-------------| - |
| `Algorithm` | Bu dosya için Özeti hesaplamak için kullanılan algoritma. Şu anda tarafından [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] `http://www.w3.org/2000/09/xmldsig#sha1`kullanılan tek değer. |

### <a name="dsigdigestvalue"></a>dsig: DigestValue
 Öğesi, `hash` öğesinin gerekli bir alt öğesidir. `dsig:DigestValue` `dsig:DigestValue` Öğesinde hiç öznitelik yok. Metin değeri, belirtilen dosya için hesaplanan karmadır.

## <a name="remarks"></a>Açıklamalar
 Uygulamanız tarafından kullanılan tüm derlemeler karşılık gelen `dependency` bir öğeye sahip olmalıdır. Bağımlı derlemeler, genel derleme önbelleğinde platform derlemeleri olarak önceden yüklenmiş olması gereken derlemeleri içermez.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir `dependency` [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama bildirimindeki öğeleri gösterir. Bu kod örneği, [ClickOnce uygulama bildirimi](../deployment/clickonce-application-manifest.md) konusu için sağlanmış daha büyük bir örneğin bir parçasıdır.

```xml
<dependency>
  <dependentOS>
    <osVersionInfo>
      <os
        majorVersion="4"
        minorVersion="10"
        buildNumber="0"
        servicePackMajor="0" />
    </osVersionInfo>
  </dependentOS>
</dependency>
<dependency>
  <dependentAssembly
    dependencyType="preRequisite"
    allowDelayedBinding="true">
    <assemblyIdentity
      name="Microsoft.Windows.CommonLanguageRuntime"
      version="4.0.20506.0" />
  </dependentAssembly>
</dependency>

<dependency>
  <dependentAssembly
    dependencyType="install"
    allowDelayedBinding="true"
    codebase="MyApplication.exe"
    size="4096">
    <assemblyIdentity
      name="MyApplication"
      version="1.0.0.0"
      language="neutral"
      processorArchitecture="x86" />
    <hash>
      <dsig:Transforms>
        <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />
      </dsig:Transforms>
      <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />
      <dsig:DigestValue>DpTW7RzS9IeT/RBSLj54vfTEzNg=</dsig:DigestValue>
    </hash>
  </dependentAssembly>
</dependency>
```

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce uygulama bildirimi](../deployment/clickonce-application-manifest.md)
- [\<Dependency > öğesi](../deployment/dependency-element-clickonce-deployment.md)