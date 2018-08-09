---
title: Acessar dados do aplicativo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], como acessar dados usando o modelo de objeto de 2003, modelos de formulário compatíveis com o InfoPath 2003, acessando dados do aplicativo
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelo do objeto do InfoPath, instanciado por meio da interface do aplicativo.
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765589"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Acessar dados do aplicativo usando o modelo de objeto do InfoPath 2003

O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado por meio da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . 
  
Um projeto de modelo de formulário do compatíveis com o InfoPath 2003 código gerenciado criado usando o Visual Studio 2012 inicializa o `thisApplication` variável no `_Startup` método da classe de código de formulário, que pode ser usado para acessar os membros da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . No exemplo a seguir, as propriedades de [nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) e a [versão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) são usadas para retornar o número de nome e a versão da instância em execução do InfoPath. Essas informações são exibidas em uma caixa de mensagem usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) . 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

No exemplo Visual c#, a referência para a `\n` caractere na cadeia de caracteres para a mensagem de alerta é processada pelo InfoPath código não gerenciado como um padrão de linha feed que faz com que o texto se quebram e ser colocada em uma nova linha na caixa de mensagem nova. Para usar explicitamente o novo valor de linha definido para o ambiente atual e a plataforma, use a propriedade **Environment.NewLine** em vez disso, conforme mostrado no exemplo a seguir. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Acessando dados do documento XML subjacente de um formulário

Os desenvolvedores podem usar a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para acessar informações sobre o documento XML subjacente de um formulário, incluindo uma referência para um XML DOM Document Object Model () que contém a fonte de dados XML do formulário. 
  
No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados que estão disponíveis a partir da interface de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , como se o documento XML subjacente foi alterado (usando a propriedade [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) e se ele tiver sido assinado digitalmente (usando a propriedade [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). A próxima caixa de mensagem usa a propriedade de [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) da interface para exibir a origem XML do documento XML de base do formulário. 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

A propriedade **xml** usada no exemplo anterior é uma propriedade do XML DOM Document Object Model (). Para obter mais informações sobre o DOM XML, consulte a documentação do SDK MSXML 5.0. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Acessando dados de arquivo de definição de formulário de um formulário

Informações sobre o arquivo. xsf de um formulário, incluindo uma referência DOM XML à fonte de dados XML que ele contém, também podem ser acessadas usando a interface de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Essa informação é acessada por meio da propriedade de [solução](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , que retorna uma referência para a interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) . 
  
No exemplo a seguir, o primeiro alerta exibe alguns dos dados que está disponíveis por meio da interface de [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , como seu local de identificador de recurso uniforme (URI) (usando a propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) e seu número de versão (usando o [ Versão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) propriedade). O alerta seguinte usa a propriedade de [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) da interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para exibir a origem XML do arquivo. xsf. 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


