---
title: Acessar dados de formulário usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- interface XDocument [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, acessando dados de formulário, XDocumentsCollection interface [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath oferece suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da interface XDocument em associação à interface XDocumentsCollection.
ms.openlocfilehash: 803122c6c377686a85f11cf48b76876c056f2ec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303672"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>Acessar dados de formulário usando o modelo de objeto do InfoPath 2003

Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath oferece suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) em associação à interface [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) . 
  
A interface **XDocument** é um dos tipos mais úteis no modelo de objeto do InfoPath porque fornece uma variedade de propriedades, métodos e eventos que não só interagem com o documento XML subjacente de um formulário, mas também executam muitas das ações que estão disponíveis na interface do usuário do InfoPath. Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, uma variável do tipo **XDocument** que `thisXDocument` é nomeada é automaticamente definida `_StartUp` no método da classe que contém manipuladores de eventos no código de formulário do seu projeto . Você pode usar a `thisXDocument` variável no código do seu formulário para acessar a interface **XDocument** e seus membros. 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>Visão geral da interface XDocumentsCollection

A interface **XDocumentsCollection** fornece os seguintes métodos e propriedades que os desenvolvedores de formulários podem usar para gerenciar os objetos **XDocument** contidos na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx)  <br/> |Fecha o formulário especificado.  <br/> |
|[Novo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) método  <br/> |Cria um novo formulário com base em um formulário existente.  <br/> |
|Método [NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx)  <br/> |Cria um novo formulário com base em um modelo de formulário existente.  <br/> |
|Método [NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx)  <br/> |Cria um novo formulário do InfoPath usando os dados XML e o modelo de formulário especificados.  <br/> |
|Método [Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx)  <br/> |Abre o formulário especificado.  <br/> |
|Propriedade [Contagem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx)  <br/> |Retorna uma contagem do número de objetos **XDocument** contidos na coleção.  <br/> |
|Propriedade[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx)  <br/> |Retorna uma referência ao objeto **XDocument** especificado.  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>Visão geral da interface XDocument

A interface **XDocument** fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir com o e realizar ações no documento XML subjacente de um formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx)  <br/> |Retorna o valor da cadeia de caracteres de uma variável de dados especificada.  <br/> |
|Método [GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx)  <br/> |Retorna uma referência ao modelo de objeto de documento XML (DOM) associado ao objeto **DataObject** especificado.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) Método ImportFile  <br/> |Importa (ou mescla) o formulário especificado com o formulário aberto no momento.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) Método PrintOut  <br/> |ImPrime o modo de exibição atual de um formulário.  <br/> |
|Método [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx)  <br/> |Recupera dados de um adaptador de dados associado de um formulário.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx)  <br/> |Salva o formulário aberto no momento.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx)  <br/> |Salva o formulário atualmente aberto com o nome especificado.  <br/> |
|Método [SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx)  <br/> |Define o valor de uma variável de dados especificada.  <br/> |
|Método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx)  <br/> |Envia um formulário de acordo com a operação de envio estabelecida no modo de design.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) Propriedade DataObjects  <br/> |Retorna uma referência à coleção **** DataObjects.  <br/> |
|Propriedade [dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML que é preenchido com os dados XML de origem de um formulário.  <br/> |
|Propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx)  <br/> |Retorna uma referência à coleção **Errors** .  <br/> |
|Propriedade [Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx)  <br/> |Retorna uma referência a um objeto que representa todas as funções e variáveis contidas em um arquivo de código de formulário.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) Propriedade IsDirty  <br/> |Retorna um valor **Boolean** que indica se os dados no formulário foram alterados.  <br/> |
|Propriedade [IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx)  <br/> |Retorna um valor **Boolean** que indica se o Dom XML está definido como somente leitura.  <br/> |
|Propriedade [IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx)  <br/> |Retorna um valor **Boolean** que indica se o formulário foi salvo após sua criação.  <br/> |
|Propriedade [IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx)  <br/> |Retorna um valor **Boolean** que indica se o formulário está no modo somente leitura.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) Propriedade IsSigned  <br/> |Retorna um valor **Boolean** que indica se o formulário é assinado digitalmente.  <br/> |
|Propriedade [Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx)  <br/> |Especifica ou retorna o valor da cadeia de caracteres do idioma usado para o formulário.  <br/> |
|Propriedade [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto adaptador de dados.  <br/> |
|Propriedade [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx)  <br/> |Retorna uma referência ao objeto **Solution** .  <br/> |
|Propriedade [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)  <br/> |Retorna uma referência ao objeto **UI** .  <br/> |
|Propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx)  <br/> |Retorna um valor String que contém o URI (Uniform Resource Identifier) do formulário.  <br/> |
|Propriedade [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx)  <br/> |Retorna uma referência ao objeto **View** .  <br/> |
|Propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx)  <br/> |Retorna uma referência à coleção **ViewInfos** .  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>Usando a coleção XDocuments e as interfaces XDocument

A interface **XDocumentsCollection** é acessada por meio da propriedade [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocumentsCollection** usando `thisApplication` a variável que é instanciada no `_StartUp` método do código de formulário do seu projeto. As linhas de código a seguir criam uma variável que faz referência à interface **XDocumentsCollection** do projeto atual. 
  
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

Em um projeto de código gerenciado criado usando o modelo de objeto compatível com o InfoPath 2003, você pode acessar a interface **XDocument** usando `thisXDocument` a variável que é instanciada no `StartUp` método do código de formulário do seu projeto. A linha de código a seguir usa `thisXDocument` a variável para acessar a interface **XDocument** do projeto atual para exibir o URI do formulário atualmente aberto em uma mensagem de alerta. 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> Quando você usa a interface **XDocument** para acessar o documento XML subjacente de um formulário, você está acessando o documento XML que está associado ao formulário atualmente aberto. 
  
Uma propriedade de chave da interface **XDocument** é a propriedade **dom** . Essa propriedade retorna uma referência ao DOM XML que é preenchido com os dados XML de origem de um formulário. Ao usar a propriedade **dom** , você pode usar qualquer uma das propriedades e métodos que são suportados pelo dom XML. Por exemplo, o código a seguir usa a propriedade **XML** do Dom XML para retornar e exibir todo o conteúdo do documento XML subjacente de um formulário. 
  
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
> Para saber mais sobre o DOM XML e todas as propriedades e os métodos aos quais ele oferece suporte, consulte o SDK do MSXML no MSDN. 
  

