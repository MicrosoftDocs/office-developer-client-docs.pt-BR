---
title: Acessar dados de aplicativo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], acessando dados usando o modelo de objeto 2003, modelos de formulário compatíveis com InfoPath 2003, acessando dados de aplicativo
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (.xsf). Esses dados são acessados por meio do objeto de nível superior na hierarquia do modelo de objeto do InfoPath, que é instariada usando a interface de aplicativo.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437438"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Acessar dados de aplicativo usando o modelo de objeto do InfoPath 2003

O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (.xsf). Esses dados são acessados por meio do objeto de nível superior na hierarquia do modelo de objeto do InfoPath, que é instariada usando a interface [de aplicativo.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) 
  
Um projeto de modelo de formulário de código gerenciado compatível com o InfoPath 2003 criado usando o Visual Studio 2012 inicializa a variável no método da classe de código de formulário, que pode ser usada para acessar os membros da interface do `thisApplication` `_Startup` aplicativo. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) No exemplo a seguir, as propriedades [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) e [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) da interface [application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) são usadas para retornar o nome e o número da versão da instância em execução do InfoPath. Essas informações são exibidas em uma caixa de mensagem usando o [método Alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UI2.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

No exemplo do Visual C#, a referência ao caractere na cadeia de caracteres da mensagem de alerta é renderizada pelo código não-managedo do InfoPath como um feed de nova linha padrão que faz com que o texto seja quebre e seja colocado em uma nova linha na caixa de  `\n` mensagem. Para usar explicitamente o novo valor de linha definido para o ambiente e a plataforma atuais, use a propriedade **Environment.NewLine,** conforme mostrado no exemplo a seguir. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Acessando dados do documento XML subjacente de um formulário

Os desenvolvedores podem usar a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para obter acesso a informações sobre o documento XML subjacente de um formulário, incluindo uma referência a um DOM (Modelo de Objeto de Documento XML) que contém os dados XML de origem do formulário. 
  
No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados disponíveis na interface [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) como se o documento XML subjacente foi alterado (usando a propriedade [IsDirty)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) e se ele foi assinado digitalmente (usando a propriedade [IsSigned).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) A próxima caixa de mensagem usa a propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para exibir o XML de origem do documento XML subjacente do formulário. 
  
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

A **propriedade xml** usada no exemplo anterior é uma propriedade do MODELO de Objeto de Documento XML (DOM). Para obter mais informações sobre o DOM XML, consulte a documentação do SDK do MSXML 5.0. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Acessando dados do arquivo de definição de formulário de um formulário

As informações sobre o arquivo .xsf de um formulário, incluindo uma referência de DOM XML aos dados XML de origem que ele contém, também podem ser acessadas usando a interface [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Essas informações são acessadas usando [a propriedade Solution,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) que retorna uma referência à interface [SolutionObject.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) 
  
No exemplo a seguir, o primeiro alerta exibe alguns dos dados disponíveis por meio da interface [SolutionObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) como o local do URI (Uniform Resource Identifier) (usando a propriedade [URI)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) e seu número de versão (usando a propriedade [Version).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) O próximo alerta usa a [propriedade DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) da interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para exibir o XML de origem do arquivo .xsf. 
  
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


