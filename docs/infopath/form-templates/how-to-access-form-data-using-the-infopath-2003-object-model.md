---
title: Acessar dados de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- interface xdocument [infopath 2007],modelos de formulário compatíveis com o InfoPath 2003, acessando dados de formulário, interface XDocumentsCollection [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath dá suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da interface XDocument em associação com a interface XDocumentsCollection.
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416472"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Acessar dados de formulário usando o modelo de objeto do InfoPath 2003

Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath dá suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) em associação com a interface [XDocumentsCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) 
  
A interface **XDocument** é um dos tipos mais úteis no modelo de objeto do InfoPath porque fornece uma variedade de propriedades, métodos e eventos que não apenas interagem com o documento XML subjacente de um formulário, mas também executam muitas das ações disponíveis na interface do usuário do InfoPath. Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, uma variável do tipo **XDocument** nomeada é automaticamente definida no método da classe que contém manipuladores de eventos no código de formulário do seu  `thisXDocument`  `_StartUp` projeto. Você pode usar  `thisXDocument` a variável no código do formulário para acessar a interface **XDocument** e seus membros. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Visão geral da interface XDocumentsCollection

A interface **XDocumentsCollection** fornece os seguintes métodos e propriedades que os desenvolvedores de formulário podem usar para gerenciar os objetos **XDocument** que a coleção contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Fecha o formulário especificado.  <br/> |
|[Novo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) método  <br/> |Cria um novo formulário com base em um formulário existente.  <br/> |
|[Método NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Cria um novo formulário com base em um modelo de formulário existente.  <br/> |
|[Método NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Cria um novo formulário do InfoPath usando os dados XML e o modelo de formulário especificados.  <br/> |
|[Método Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Abre o formulário especificado.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Retorna uma contagem do número de **objetos XDocument** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Retorna uma referência ao objeto **XDocument** especificado.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Visão geral da interface XDocument

A interface **XDocument** fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir e executar ações no documento XML subjacente de um formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Método GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Retorna o valor da cadeia de caracteres de uma variável de dados especificada.  <br/> |
|[Método GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Retorna uma referência ao DOM (Modelo de Objeto de Documento) XML associado ao objeto **DataObject** especificado.  <br/> |
|[Método ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx)  <br/> |Importa (ou mescla) o formulário especificado com o formulário aberto no momento.  <br/> |
|[Método PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx)  <br/> |Imprime o atual de um formulário.  <br/> |
|[Método Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Recupera dados do adaptador de dados associado de um formulário.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Salva o formulário aberto no momento.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Salva o formulário aberto no momento com o nome especificado.  <br/> |
|[Método SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Define o valor de uma variável de dados especificada.  <br/> |
|Método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Envia um formulário de acordo com a operação de envio estabelecida no modo de design.  <br/> |
|[Propriedade DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx)  <br/> |Retorna uma referência à **coleção DataObjects** .  <br/> |
|[Propriedade DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML que é preenchido com os dados XML de origem de um formulário.  <br/> |
|Propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx)  <br/> |Retorna uma referência à **coleção Errors** .  <br/> |
|Propriedade [Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Retorna uma referência a um objeto que representa todas as funções e variáveis contidas em um arquivo de código de formulário.  <br/> |
|[Propriedade IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx)  <br/> |Retorna um **valor Boolean** indicando se os dados no formulário foram alterados.  <br/> |
|[Propriedade IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Retorna um **valor Boolean** que indica se o DOM XML está definido como somente leitura.  <br/> |
|[Propriedade IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Retorna um **valor Boolean** que indica se o formulário foi salvo após sua criação.  <br/> |
|[Propriedade IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Retorna um **valor Boolean** indicando se o formulário está no modo somente leitura.  <br/> |
|[Propriedade IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx)  <br/> |Retorna um **valor Boolean** indicando se o formulário é assinado digitalmente.  <br/> |
|[Propriedade Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Especifica ou retorna o valor da cadeia de caracteres do idioma usado para o formulário.  <br/> |
|[Propriedade QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto do adaptador de dados.  <br/> |
|[Propriedade Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Retorna uma referência ao **objeto Solution** .  <br/> |
|[Propriedade da interface do](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) usuário  <br/> |Retorna uma referência ao objeto **de interface do** usuário.  <br/> |
|[Propriedade URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Retorna um valor de cadeia de caracteres que contém o URI (Uniform Resource Identifier) do formulário.  <br/> |
|[Propriedade View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx)  <br/> |Retorna uma referência ao **objeto View** .  <br/> |
|Propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Retorna uma referência à **coleção ViewInfos** .  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Usando a coleção XDocuments e as interfaces XDocument

A interface **XDocumentsCollection** é acessada por meio da propriedade [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) da interface [application.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocumentsCollection** usando a variável instariada no método do código de formulário do seu  `thisApplication`  `_StartUp` projeto. As linhas de código a seguir criam uma variável que faz referência à interface **XDocumentsCollection** do projeto atual. 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocument** usando a variável instariada no método do código de formulário do seu  `thisXDocument`  `StartUp` projeto. A linha de código a seguir usa a variável para acessar  `thisXDocument` a interface **XDocument** do projeto atual para exibir o URI do formulário aberto no momento em uma mensagem de alerta. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Ao usar a interface **XDocument** para acessar o documento XML subjacente de um formulário, você está acessando o documento XML associado ao formulário aberto no momento. 
  
Uma propriedade chave da interface **XDocument** é a **propriedade DOM.** Essa propriedade retorna uma referência ao DOM XML que é preenchido com os dados XML de origem de um formulário. Ao usar a **propriedade DOM,** você pode usar qualquer uma das propriedades e métodos que são suportados pelo DOM XML. Por exemplo, o código a seguir usa a propriedade **xml** do DOM XML para retornar e exibir todo o conteúdo do documento XML subjacente de um formulário. 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> Para saber mais sobre o DOM XML e todas as propriedades e métodos compatíveis, consulte o SDK do MSXML no MSDN. 
  

