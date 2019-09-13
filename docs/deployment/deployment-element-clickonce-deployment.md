---
title: '&lt;Dağıtım&gt; öğesi (ClickOnce dağıtımı) | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- urn:schemas-microsoft-com:asm.v2#subscription
- urn:schemas-microsoft-com:asm.v2#beforeApplicationStartup
- urn:schemas-microsoft-com:asm.v2#deploymentProvider
- urn:schemas-microsoft-com:asm.v2#update
- urn:schemas-microsoft-com:asm.v2#deployment
- urn:schemas-microsoft-com:asm.v2#expiration
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <deployment> element [ClickOnce deployment manifest]
ms.assetid: 4fafa9c2-97a0-4cea-b8fd-9746dca33af4
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 988ce0859ab24377395cc4077f9e6fa42e0487a5
ms.sourcegitcommit: 4dfe098ac0df294aad63e6b384d6575980798ca3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70887862"
---
# <a name="ltdeploymentgt-element-clickonce-deployment"></a>&lt;Dağıtım&gt; öğesi (ClickOnce dağıtımı)
Güncelleştirmelerin dağıtımı için kullanılan öznitelikleri ve sistemde pozlandırmayı tanımlar.

## <a name="syntax"></a>Sözdizimi

```xml

      <deployment
   install
   minimumRequiredVersion
   mapFileExtensions
   disallowUrlActivation
   trustUrlParameters
>
   <subscription>
         <update>
            <beforeApplicationStartup/>
            <expiration
               maximumAge
               unit
            />
         </update>
   </subscription>
   <deploymentProvider
      codebase
   />
</deployment>
```

## <a name="elements-and-attributes"></a>Öğeler ve öznitelikler
 Öğesi gereklidir ve `urn:schemas-microsoft-com:asm.v2` ad alanında bulunur. `deployment` Öğesi aşağıdaki özniteliklere sahiptir.

| Öznitelik | Açıklama |
|--------------------------| - |
| `install` | Gerekli. Bu uygulamanın Windows **Başlat** menüsünde ve Denetim Masası **Program Ekle veya Kaldır** uygulamasında bir varlığı tanımlayıp tanımlamadığını belirtir. Geçerli değerler ve `true` ' `false`dir. , Her zaman bu uygulamanın en son sürümünü ağdan çalıştırır `subscription` ve öğesini tanımaz. [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] `false` |
| `minimumRequiredVersion` | İsteğe bağlı. Bu uygulamanın istemcide çalışabilecek en düşük sürümünü belirtir. Uygulamanın sürüm numarası dağıtım bildiriminde sağlanan sürüm numarasından azsa, uygulama çalışmaz. Sürüm numaraları biçiminde `N.N.N.N`belirtilmelidir, burada `N` işaretsiz bir tamsayıdır. Özniteliği ise `false` ,`minimumRequiredVersion`ayarlanmamalıdır. `install` |
| `mapFileExtensions` | İsteğe bağlı. Varsayılan olarak `false`. Eğer `true`, dağıtımdaki tüm dosyaların. deploy uzantısı olmalıdır. [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)], bu uzantıyı Web sunucusundan indirdiği anda bu dosyaların dışına çıkaracaktır. Kullanarak [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]uygulamanızı yayımlarsanız, bu uzantıyı otomatik olarak tüm dosyalara ekler. Bu parametre, bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] dağıtım içindeki tüm dosyaların,. exe gibi "güvenli olmayan" uzantılar ile biten dosyaların aktarımını engelleyen bir Web sunucusundan indirilmesine izin verir. |
| `disallowUrlActivation` | İsteğe bağlı. Varsayılan olarak `false`. `true`, Yüklü bir uygulamanın URL 'ye tıklanması veya URL 'yi Internet Explorer 'a girerek başlatılmasını önler. `install` Özniteliği yoksa, bu öznitelik yoksayılır. |
| `trustURLParameters` | İsteğe bağlı. Varsayılan olarak `false`. İse `true`, URL 'nin uygulamaya geçirilen sorgu dizesi parametreleri içermesini sağlar ve komut satırı bağımsız değişkenleri bir komut satırı uygulamasına geçirilir. Daha fazla bilgi için [nasıl yapılır: Sorgu dizesi bilgilerini çevrimiçi ClickOnce uygulamasında](../deployment/how-to-retrieve-query-string-information-in-an-online-clickonce-application.md)alma.<br /><br /> `false`Özniteliği ise `true` ,`trustUrlParameters` bildirimden dışlanması ya da açıkça olarak ayarlanması gerekir. `disallowUrlActivation` |

 `deployment` Öğesi de aşağıdaki alt öğeleri içerir.

## <a name="subscription"></a>subscription
 İsteğe bağlı. `update` Öğesini içerir. `subscription` Öğesinde hiç öznitelik yok. `subscription` Öğe yoksa[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] , uygulama güncelleştirmeleri hiçbir şekilde taramayacaktır. `install` Öğesininözniteliği`false`ise, ağdan başlatılan bir[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama her zaman en son sürümü kullandığından, öğeyoksayılır.`subscription` `deployment`

## <a name="update"></a>update
 Gerekli. Bu öğe, `subscription` öğesinin bir alt öğesidir ve ya da `expiration` öğesini içerir `beforeApplicationStartup` . `beforeApplicationStartup``expiration` aynı dağıtım bildiriminde her ikisi de belirtilemez.

 `update` Öğesinde hiç öznitelik yok.

## <a name="beforeapplicationstartup"></a>beforeApplicationStartup
 İsteğe bağlı. Bu öğe, `update` öğesinin bir alt öğesidir ve özniteliği yoktur. Öğe mevcut olduğunda, istemci çevrimiçi ise güncelleştirmeleri [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] denetlediğinde uygulama engellenir. `beforeApplicationStartup` Bu öğe yoksa, [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] önce `expiration` öğe için belirtilen değerlere göre güncelleştirmeleri tarar. `beforeApplicationStartup``expiration` aynı dağıtım bildiriminde her ikisi de belirtilemez.

## <a name="expiration"></a>Dolmadan
 İsteğe bağlı. Bu öğe, `update` öğesinin bir alt öğesidir ve alt öğesi yoktur. `beforeApplicationStartup``expiration` aynı dağıtım bildiriminde her ikisi de belirtilemez. Güncelleştirme denetimi gerçekleştiğinde ve güncelleştirilmiş bir sürüm algılandığında, varolan sürüm çalışırken yeni sürüm önbelleğe alınır. Yeni sürüm daha sonra [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamanın bir sonraki başlatmaya yüklenir.

 `expiration` Öğesi aşağıdaki öznitelikleri destekler.

|Öznitelik|Açıklama|
|---------------|-----------------|
|`maximumAge`|Gerekli. Uygulamanın bir güncelleştirme denetimi gerçekleştirmeden önce geçerli güncelleştirmenin ne kadar eski olması gerektiğini tanımlar. Zaman birimi `unit` özniteliğe göre belirlenir.|
|`unit`|Gerekli. İçin `maximumAge`zaman birimini tanımlar. Geçerli birimler `hours`, `days`, ve `weeks`.|

## <a name="deploymentprovider"></a>deploymentProvider
 .NET Framework 2,0 için, dağıtım bildirimi bir `subscription` bölüm içeriyorsa bu öğe gereklidir. .NET Framework 3,5 ve üzeri için, bu öğe isteğe bağlıdır ve varsayılan olarak dağıtım bildiriminin bulunduğu sunucu ve dosya yoludur.

 Bu öğe, `deployment` öğesinin bir alt öğesidir ve aşağıdaki özniteliğe sahiptir.

| Öznitelik | Açıklama |
|------------| - |
| `codebase` | Gerekli. [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] Uygulamayı güncelleştirmek için kullanılan dağıtım bildiriminin bir Tekdüzen Kaynak tanımlayıcısı (URI) olarak konumunu tanımlar. Bu öğe Ayrıca, CD tabanlı yüklemeler için güncelleştirme konumlarına iletme olanağı tanır. Geçerli bir URI olmalıdır. |

## <a name="remarks"></a>Açıklamalar
 [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] Uygulamanızı başlangıçta güncelleştirmeleri tarayacak, başlangıçtan sonra güncelleştirmeleri taratın veya güncelleştirmeleri hiçbir şekilde denetbir şekilde kontrol edebilirsiniz. Başlangıçta güncelleştirmeleri taramak için öğesinin `beforeApplicationStartup` `update` altında bulunduğundan emin olun. Başlangıçtan sonra güncelleştirmeleri taramak için, öğesinin `expiration` `update` öğesinin altında mevcut olduğundan ve bu güncelleştirme aralıklarının sağlandığından emin olun.

 Güncelleştirme denetimini devre dışı bırakmak için `subscription` öğesini kaldırın. Güncelleştirmeleri hiçbir zaman taramayacak dağıtım bildiriminde belirttiğinizde, <xref:System.Deployment.Application.ApplicationDeployment.CheckForUpdate%2A> yöntemini kullanarak güncelleştirmeleri el ile denetleyebilirsiniz.

 DeploymentProvider 'ın güncelleştirmelerle nasıl ilişkili olduğu hakkında daha fazla bilgi için bkz. [ClickOnce Update stratejisi seçme](../deployment/choosing-a-clickonce-update-strategy.md).

## <a name="examples"></a>Örnekler
 Aşağıdaki kod örneğinde bir `deployment` [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] dağıtım bildiriminde bir öğe gösterilmektedir. Örnek, tercih edilen `deploymentProvider` güncelleştirme konumunu belirtmek için bir öğesi kullanır.

```xml
<deployment install="true" minimumRequiredVersion="2.0.0.0" mapFileExtension="true" trustUrlParameters="true">
    <subscription>
      <update>
        <expiration maximumAge="6" unit="hours" />
      </update>
    </subscription>
    <deploymentProvider codebase="http://www.adatum.com/MyApplication.application" />
  </deployment>
```

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce dağıtım bildirimi](../deployment/clickonce-deployment-manifest.md)