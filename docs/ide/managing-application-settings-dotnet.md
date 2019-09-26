---
title: Uygulama ayarlarını yönetme (.NET)
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- msvse_settingsdesigner.err.nameblank
helpviewer_keywords:
- application settings [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0627a96bf100232987ace5a42430310912f97b8c
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252084"
---
# <a name="manage-application-settings-net"></a>Uygulama ayarlarını yönetme (.NET)

Uygulama ayarları, uygulama bilgilerini dinamik olarak depolamanızı sağlar. Ayarları, uygulama kodunda (örneğin bir bağlantı dizesi), kullanıcı tercihlerine ve çalışma zamanında gereken diğer bilgilere dahil edilmemelidir. istemci bilgisayarda bilgi depolamanıza olanak tanır.

Uygulama ayarları, Visual Studio 'nun önceki sürümlerinde kullanılan dinamik özelliklerin yerini alır.

Her uygulama ayarının benzersiz bir adı olmalıdır. Ad, harf, sayı veya sayı ile başlamamayan alt çizginin herhangi bir birleşimi olabilir ve boşluk içeremez. Ad, `Name` özelliği aracılığıyla değiştirilir.

Uygulama ayarları, XML `TypeConverter` 'e serileştirilmiş veya uygulayan `ToString` / `FromString`bir veri türü olarak depolanabilir. En yaygın `String`türler, `Integer`, ve `Boolean` <xref:System.Object>' dir, ancak değerleri ,veyabirbağlantıdizesiolarakdadepolayabilirler.<xref:System.Drawing.Color>

Uygulama ayarları da bir değer tutar. Değer, **Value** özelliği ile ayarlanır ve ayarın veri türüyle eşleşmelidir.

Ayrıca, uygulama ayarları, tasarım zamanında bir formun veya denetimin özelliğine bağlanabilir.

Kapsama göre iki tür uygulama ayarı vardır:

- Uygulama kapsamlı ayarlar, bir Web hizmeti URL 'SI veya bir veritabanı bağlantı dizesi gibi bilgiler için kullanılabilir. Bu değerler uygulamayla ilişkilendirilir. Bu nedenle, kullanıcılar çalışma zamanında bunları değiştiremezler.

- Kullanıcı kapsamlı ayarlar, bir formun veya yazı tipi tercihinin son konumunu kalıcı hale getirme gibi bilgiler için kullanılabilir. Kullanıcılar, çalışma zamanında bu değerleri değiştirebilir.

**Kapsam** özelliğini kullanarak bir ayarın türünü değiştirebilirsiniz.

Proje sistemi uygulama ayarlarını iki XML dosyasında depolar:

- ilk uygulama ayarını oluştururken tasarım zamanında oluşturulan bir *app. config* dosyası

- uygulamayı çalıştıran kullanıcı herhangi bir kullanıcı ayarının değerini değiştirdiğinde çalışma zamanında oluşturulan bir *User. config* dosyası.

Uygulama özellikle bunu yapmak için bir yöntem çağırmadığı takdirde Kullanıcı ayarlarındaki değişikliklerin diske yazılmadığından emin olun.

## <a name="create-application-settings-at-design-time"></a>Tasarım zamanında uygulama ayarları oluşturma

Tasarım zamanında, uygulama ayarlarını iki şekilde oluşturabilirsiniz: **Proje Tasarımcısı**'nın **Ayarlar** sayfasını veya bir form veya denetim için **Özellikler** penceresini kullanarak bir özelliği bir özelliğe bağlamanıza olanak tanır.

Uygulama kapsamlı bir ayar oluşturduğunuzda (örneğin, bir veritabanı bağlantı dizesi veya sunucu kaynaklarına bir başvuru), [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] `<applicationSettings>` etiketi ile *app. config dosyasına* kaydeder. (Bağlantı dizeleri `<connectionStrings>` etiketinin altına kaydedilir.)

Kullanıcı kapsamlı bir ayar oluşturduğunuzda (örneğin, varsayılan yazı tipi, giriş sayfası veya pencere boyutu), [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] `<userSettings>` etiketi ile *app. config dosyasına* kaydeder.

> [!IMPORTANT]
> Bağlantı dizelerini *app. config*' de depoladığınızda, bağlantı dizesinde parolalar veya sunucu yolları gibi hassas bilgilerin görüntülenmesinden kaçınmak için önlemler almalısınız.
>
> Bir dış kaynaktan bir kullanıcı KIMLIĞI ve parola sağlayan bir bağlantı dizesi bilgileri alırsanız, Bağlantı dizenizi oluşturmak için kullandığınız değerlerin ek bağlantı dizesi parametreleri içermediğinden emin olmak için dikkatli olmanız gerekir Bu, bağlantınızın davranışını değiştirir.
>
> Yapılandırma dosyasındaki hassas bilgileri şifrelemek için korumalı yapılandırma özelliğini kullanmayı düşünün. Daha fazla bilgi için bkz. [bağlantı bilgilerini koruma](/dotnet/framework/data/adonet/protecting-connection-information).

> [!NOTE]
> Sınıf kitaplıkları için yapılandırma dosyası modeli olmadığından, sınıf kitaplığı projeleri için uygulama ayarları uygulanmaz. Özel durum, bir yapılandırma dosyası olabilen Office DLL projesi için bir Visual Studio Araçları.

## <a name="use-customized-settings-files"></a>Özelleştirilmiş ayarlar dosyalarını kullan

Ayar gruplarının kolay yönetimi için projenize özelleştirilmiş ayarlar dosyaları ekleyebilirsiniz. Tek bir dosyada bulunan ayarlar bir birim olarak yüklenir ve kaydedilir. Ayarları, sık kullanılan ve seyrek kullanılan gruplar için ayrı dosyalarda depolamak, ayarları yükleme ve kaydetme sırasında zamandan tasarruf edebilir.

Örneğin, projenize *SpecialSettings. Settings* gibi bir dosya ekleyebilirsiniz. Sınıfınız ad alanında gösterilmediğinden `Partial Class SpecialSettings` **, görünüm kodu** içeren özel ayarlar dosyasını okuyabilir. `My` `SpecialSettings`

**Ayarlar Tasarımcısı** öncelikle proje sisteminin oluşturduğu *Settings. Settings* dosyasını arar; Bu dosya, **Proje Tasarımcısı** 'nın **Ayarlar** sekmesinde görüntülediği varsayılan dosyadır. *Settings. Settings* , projeler için [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] *My projem* klasöründe ve projeler için [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] *Özellikler* klasöründe bulunur. **Proje Tasarımcısı** daha sonra projenin kök klasöründeki diğer ayarlar dosyalarını arar. Bu nedenle, özel ayarlar dosyanızı buraya koymanız gerekir. Projeniz başka bir yerde bir *. Settings* dosyası eklerseniz, **Proje Tasarımcısı** bunu bulamaz.

## <a name="access-or-change-application-settings-at-run-time-in-visual-basic"></a>Visual Basic çalışma zamanında uygulama ayarlarını erişim veya değiştirme

Visual Basic projelerinde, `My.Settings` nesnesini kullanarak çalışma zamanında uygulama ayarlarına erişebilirsiniz. **Ayarlar sayfasında,** *Settings. vb* dosyasını görüntülemek için **kodu görüntüle** düğmesine tıklayın. *Settings. vb* , ayarlar `Settings` <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> <xref:System.Configuration.ApplicationSettingsBase.PropertyChanged> sınıfındabu<xref:System.Configuration.ApplicationSettingsBase.SettingsSaving>olayları idare etmenizi sağlayan sınıfını tanımlar:, ,ve.<xref:System.Configuration.ApplicationSettingsBase.SettingsLoaded> *Settings. vb* dosyasındaki sınıfın,tümoluşturulansınıfıdeğilyalnızcakullanıcıyaaitkodugörüntüleyenkısmibirsınıfolduğunuunutmayın.`Settings` `My.Settings` Nesnesini kullanarak uygulama ayarlarına erişme hakkında daha fazla bilgi için bkz. [erişim uygulama ayarları (.NET Framework)](/dotnet/visual-basic/developing-apps/programming/app-settings/accessing-application-settings).

Kullanıcının çalışma zamanında değiştiği kullanıcı kapsamlı ayarların değerleri (örneğin, bir formun konumu) bir *User. config* dosyasında depolanır. Varsayılan değerlerin *app. config dosyasına*hala kaydedildiğine dikkat edin.

Çalışma zamanında Kullanıcı tanımlı herhangi bir ayar değiştirilmişse, örneğin, uygulamayı test etmek ve bu ayarları varsayılan değerlerine sıfırlamak istiyorsanız, **Synchronize** düğmesine tıklayın.

Ayarlara erişmek için `My.Settings` nesneyi ve Default *. Settings* dosyasını kullanmanızı önemle tavsiye ederiz. Bunun nedeni, ayarlara Özellikler atamak için **Ayarlar tasarımcısını** kullanabilir ve ek olarak, Uygulama kapanmadan önce Kullanıcı ayarları otomatik olarak kaydedilir. Ancak, Visual Basic uygulamanız ayarlara doğrudan erişebilir. Bu durumda, `MySettings` sınıfa erişmeniz ve projenin kökünde özel bir *. Settings* dosyası kullanmanız gerekir. Uygulama için C# yaptığınız gibi Kullanıcı ayarlarını uygulamayı sonlandırmadan önce kaydetmelisiniz; Bu, aşağıdaki bölümde açıklanmıştır.

<!-- markdownlint-disable MD003 MD020 -->
## <a name="access-or-change-application-settings-at-run-time-in-c"></a>İçindeki çalışma zamanında uygulama ayarlarına erişin veya bu ayarları değiştirinC#
<!-- markdownlint-enable MD003 MD020 -->

Visual Basic C#dışındaki dillerde, aşağıdaki `Settings` [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] örnekte gösterildiği gibi, sınıfına doğrudan erişmeniz gerekir.

```csharp
Properties.Settings.Default.FirstUserSetting = "abc";
```

Kullanıcı ayarlarını kalıcı hale getirmek `Save` için bu sarmalayıcı sınıfının yöntemini açıkça çağırmanız gerekir. Bunu genellikle ana formun `Closing` olay işleyicisinde yapabilirsiniz. Aşağıdaki C# örnek `Save` yöntemine bir çağrı gösterir.

```csharp
Properties.Settings.Default.Save();
```

Uygulama ayarlarına `Settings` sınıfı aracılığıyla erişme hakkında genel bilgi için bkz. [uygulama ayarlarına genel bakış (.NET Framework)](/dotnet/framework/winforms/advanced/application-settings-overview). Ayarlar arasında yineleme yapma hakkında daha fazla bilgi için bu [Forum gönderisini](https://social.msdn.microsoft.com/Forums/vstudio/40fbb470-f1e8-4a02-a4a0-9f62b54d0fc4/is-this-possible-propertiessettingsdefault?forum=csharpgeneral)inceleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Uygulama ayarlarına erişim (.NET Framework)](/dotnet/visual-basic/developing-apps/programming/app-settings/accessing-application-settings)
