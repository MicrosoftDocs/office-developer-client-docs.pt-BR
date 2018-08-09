---
title: Acessar dados de aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- nomes de aplicativo [infopath 2007], acessando o nome do aplicativo [InfoPath 2007], InfoPath 2007, acessando dados do aplicativo, acessando a versão do aplicativo [InfoPath 2007], [InfoPath 2007] de versões de aplicativo, IDs de idioma [InfoPath 2007], LCID [InfoPath ID de dados do aplicativo [InfoPath 2007], acessando o idioma de 2007], [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: O InfoPath modelo de objeto de código gerenciado fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado, usando a classe de aplicativo.
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765591"
---
# <a name="access-application-data"></a>Acessar dados de aplicativo

O InfoPath modelo de objeto de código gerenciado fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado, usando a classe de [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
Em um projeto do InfoPath código gerenciado formulário modelo criado usando o Visual Studio 2012, você pode usar a **Este** (c#) ou palavra-chave **Me** (Visual Basic) para acessar uma instância da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que representa o aplicativo atual do InfoPath, que podem ser usados para acessar as propriedades e métodos da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
## <a name="example"></a>Exemplo

### <a name="displaying-the-application-name-version-and-language-id"></a>Exibir o nome do aplicativo, versão e ID de idioma

No exemplo a seguir, as propriedades de [nome](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) e a [versão](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) são usadas para retornar o número de nome e a versão da instância em execução do InfoPath. A propriedade [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) , em seguida, é usada para retornar um objeto **LanguageSettings** , que por sua vez, é usado para retornar o LCID (um número de quatro dígitos) para o idioma que está sendo usado atualmente para o idioma de interface de usuário do InfoPath. Finalmente, todas estas informações é exibido em uma caixa de mensagem. 
  
> [!IMPORTANT]
> Para a propriedade **LanguageSettings** funcionar, você deve estabelecer uma referência à biblioteca de objeto do Microsoft Office 14.0 da guia **COM** da caixa de diálogo **Adicionar referência** no Visual Studio 2012. Isso irá estabelecer uma referência para o namespace da **Microsoft.Office.Core** , que contém a classe **LanguageSettings** . Além disso, o formulário deve estar executando como confiança total. 
  
Este exemplo requer um **usando** ou a diretiva de **importações** para o namespace da **Microsoft.Office.Core** na seção Declaração do módulo do formulário de código. 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


