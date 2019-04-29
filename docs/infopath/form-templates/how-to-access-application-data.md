---
title: Acessar dados de aplicativo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- nomes de aplicativos [InfoPath 2007], acessando o nome do aplicativo [InfoPath 2007], InfoPath 2007, acessar dados de aplicativos, acessar a versão do aplicativo [InfoPath 2007], versões de aplicativos [InfoPath 2007], IDs de idioma [InfoPath 2007], LCID [InfoPath 2007], dados de aplicativos [InfoPath 2007], acessando o ID de idioma [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: O modelo de objeto de código gerenciado do InfoPath fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (. xsf). Esses dados são acessados por meio do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciada usando a classe Application.
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417228"
---
# <a name="access-application-data"></a>Acessar dados de aplicativo

O modelo de objeto de código gerenciado do InfoPath fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (. xsf). Esses dados são acessados por meio do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciada usando a classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
Em um projeto de modelo de formulário de código gerenciado do InfoPath criado usando o Visual Studio 2012, você pode usar a palavra-chave **this** (C#) ou **me** (Visual Basic) para acessar uma instância da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que representa o aplicativo do InfoPath atual, que pode ser usado para acessar as propriedades e os métodos da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . 
  
## <a name="example"></a>Exemplo

### <a name="displaying-the-application-name-version-and-language-id"></a>Exibindo o nome do aplicativo, a versão e a ID de idioma

No exemplo a seguir, as propriedades [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) e [version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) são usadas para retornar o nome e o número da versão da instância em execução do InfoPath. A propriedade [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) é usada para retornar um objeto **LanguageSettings** , que por sua vez é usado para retornar o LCID (um número de quatro dígitos) para o idioma que está sendo usado no momento para o idioma da interface do usuário do InfoPath. Por fim, todas essas informações são exibidas em uma caixa de mensagem. 
  
> [!IMPORTANT]
> Para que a propriedade **LanguageSettings** funcione, você deve estabelecer uma referência à biblioteca de objetos do Microsoft Office 14,0 a partir da guia **com** da caixa de diálogo **adicionar referência** no Visual Studio 2012. Isso estabelecerá uma referência ao namespace **Microsoft. Office. Core** , que contém a classe **LanguageSettings** . Além disso, o formulário deve estar sendo executado como confiança total. 
  
Este exemplo exige uma diretiva **using** ou Imports para o namespace **Microsoft. Office. Core** na seção declaração do módulo de código do formulário. **** 
  
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


