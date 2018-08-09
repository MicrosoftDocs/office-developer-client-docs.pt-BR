---
title: Acessar dados de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- interface de XDocument [infopath 2007], modelos de formulário compatíveis com o InfoPath 2003, como acessar dados do formulário, XDocumentsCollection interface [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar informações sobre o documento XML de base do formulário, acessar os dados contidos no documento XML ou executar alguma ação no documento XML programaticamente. O modelo de objeto do InfoPath suporta acessar e manipular o documento XML subjacente de um formulário utilizando a interface XDocument em associação com a interface XDocumentsCollection.
ms.openlocfilehash: 24e9abc8ce7327ab94b3608f1279c0f0d381ea83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765605"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Acessar dados de formulário usando o modelo de objeto do InfoPath 2003

Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar informações sobre o documento XML de base do formulário, acessar os dados contidos no documento XML ou executar alguma ação no documento XML programaticamente. O modelo de objeto do InfoPath suporta acessar e manipular o documento XML subjacente de um formulário utilizando a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) em associação com a interface [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
A interface de **XDocument** é um dos tipos mais úteis no modelo de objeto do InfoPath porque ele fornece uma variedade de propriedades, métodos, e eventos que não apenas interagem com o XML subjacente de um formulário de documento, mas também executam muitas das ações que estão disponíveis na interface do usuário do InfoPath. Em um projeto de código gerenciado criado usando o modelo de objeto do InfoPath 2003 compatíveis, uma variável de digite **XDocument** nomeado `thisXDocument` será automaticamente definida no `_StartUp` método da classe que contém manipuladores de eventos no código de formulário do projeto . Você pode usar o `thisXDocument` variável no código do formulário para acessar a interface **XDocument** e seus membros. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Visão geral da Interface XDocumentsCollection

A interface **XDocumentsCollection** fornece os seguintes métodos e propriedades que os desenvolvedores de formulário podem usar para gerenciar os objetos **XDocument** contido na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Fecha o formulário especificado.  <br/> |
|Método [New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx)  <br/> |Cria um novo formulário baseado em um formulário existente.  <br/> |
|Método [NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Cria um novo formulário baseado em um modelo de formulário existente.  <br/> |
|Método [NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Cria um novo formulário do InfoPath usando o modelo de formulário e de dados XML especificado.  <br/> |
|Método [Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Abre o formulário especificado.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Retorna uma contagem do número de objetos **XDocument** contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Retorna uma referência ao objeto **XDocument** especificado.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Visão geral da Interface XDocument

A interface de **XDocument** fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com e executar ações em um documento XML subjacente de um formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Retorna o valor de cadeia de caracteres de uma variável de dados especificada.  <br/> |
|Método [getDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Retorna uma referência para o XML DOM Document Object Model () associado ao objeto **DataObject** especificado.  <br/> |
|Método [ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx)  <br/> |Importa (ou mescla) o formulário especificado com o formulário atualmente aberto.  <br/> |
|Método [printOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx)  <br/> |Imprime o modo de exibição atual de um formulário.  <br/> |
|Método [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Recupera dados do adaptador de dados associado de um formulário.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Salva o formulário atualmente aberto.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Salva o formulário atualmente aberto com o nome especificado.  <br/> |
|Método [SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Define o valor de uma variável de dados especificada.  <br/> |
|Método de [envio](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Envia um formulário de acordo com a operação de envio estabelecida no modo de design.  <br/> |
|Propriedade [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx)  <br/> |Retorna uma referência à coleção **DataObjects** .  <br/> |
|Propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML que é preenchida com a fonte de dados XML de um formulário.  <br/> |
|Propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx)  <br/> |Retorna uma referência à coleção **Errors** .  <br/> |
|Propriedade [Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Retorna uma referência a um objeto que representa todas as funções e variáveis contidas em um arquivo de código do formulário.  <br/> |
|Propriedade [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx)  <br/> |Retorna um valor **Boolean** que indica se os dados no formato foi alterados.  <br/> |
|Propriedade [IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Retorna um valor **Boolean** indicando se o DOM XML está definido como somente leitura.  <br/> |
|Propriedade [IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Retorna um valor **Boolean** que indica se o formulário foi salvo depois que ele foi criado.  <br/> |
|Propriedade [IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Retorna um valor **Boolean** que indica se o formulário está no modo somente leitura.  <br/> |
|Propriedade [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx)  <br/> |Retorna um valor **Boolean** que indica se o formulário é assinado digitalmente.  <br/> |
|Propriedade [Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Especifica ou retorna o valor de cadeia de caracteres do idioma usado para o formulário.  <br/> |
|Propriedade [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto adaptador de dados.  <br/> |
|Propriedade da [solução](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Retorna uma referência ao objeto de **solução** .  <br/> |
|Propriedade [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Retorna uma referência ao objeto de **interface do usuário** .  <br/> |
|Propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Retorna um valor string que contém o identificador de URI (Uniform Resource) do formulário.  <br/> |
|Propriedade [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx)  <br/> |Retorna uma referência ao objeto **View** .  <br/> |
|Propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Retorna uma referência à coleção **ViewInfos** .  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Usando a coleção XDocuments e as Interfaces de XDocument

A interface **XDocumentsCollection** é acessada por meio da propriedade [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocumentsCollection** usando o `thisApplication` variável é instanciado no `_StartUp` método do código de formulário do projeto. Linhas de código a seguir criam uma variável que faz referência a interface **XDocumentsCollection** do projeto atual. 
  
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

Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocument** usando o `thisXDocument` variável é instanciado no `StartUp` método do código de formulário do projeto. A seguinte linha de código usa o `thisXDocument` variável para acessar a interface **XDocument** do projeto atual para exibir o URI do formulário atualmente aberto em uma mensagem de alerta. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Quando você usa a interface **XDocument** para acessar o documento XML subjacente de um formulário, você está acessando o documento XML que está associado com o formulário atualmente aberto. 
  
Uma propriedade de chave da interface **XDocument** é a propriedade **DOM** . Essa propriedade retorna uma referência ao DOM XML que é preenchida com a fonte de dados XML de um formulário. Ao usar a propriedade **DOM** , você pode usar qualquer uma das propriedades e métodos que são compatíveis com o DOM. XML Por exemplo, o código a seguir usa a propriedade **xml** do DOM XML para retornar e exibir todo o conteúdo do documento XML subjacente de um formulário. 
  
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
> Para saber mais sobre o DOM XML e todas as propriedades e métodos que ele suporta, consulte o SDK do MSXML no MSDN. 
  

