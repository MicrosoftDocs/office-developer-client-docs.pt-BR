---
title: Acessar fontes de dados externos
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- classes de conexão de dados [infopath 2007], fontes de dados secundário [InfoPath 2007], dados [InfoPath 2007], secundários, DataSource classe [InfoPath 2007], acessando fontes de dados externas [InfoPath 2007], DataSourceCollection classe [InfoPath 2007] DataConnectionCollection classe [InfoPath 2007], DataConnection classe [InfoPath 2007], InfoPath 2007, como acessar dados externos, dados [InfoPath 2007], fontes externas
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar fontes de dados secundária do formulário e manipular os dados que elas contêm.
ms.openlocfilehash: e26708e0033bbfe4110ac522dd1e0a0dd037c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765608"
---
# <a name="access-external-data-sources"></a>Acessar fontes de dados externos

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar fontes de dados secundária do formulário e manipular os dados que elas contêm. 
  
Cada fonte de dados secundário é representado por um objeto instanciado usando a classe de [fonte de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) e corresponde aos dados armazenados, obtidos de alguma origem externa de dados, como um banco de dados ou uma consulta de serviço Web. Essas fontes de dados são referidas como secundário porque quando o usuário salvar um formulário do InfoPath, o usuário está salvando os dados somente na fonte de dados principal (ou principal), não os dados nas fontes de dados secundário. A conexão a uma fonte de dados é representado por um objeto instanciado usando uma das classes "conexão de dados", como a classe de [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , que representa uma conexão de dados para um serviço Web XML. 
  
Objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) instanciado representa o armazenamento de dados XML retornados por uma conexão de dados (de um banco de dados ou uma consulta de serviço da Web) e a classe de "conexão de dados" representa a conexão de dados em si (conforme definido e nomeado usando o **dados Conexões** command na guia **dados** ). 
  
O modelo de objeto do InfoPath suporta acesso a fontes de dados secundário de um formulário com o uso da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) em associação com a classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) . 
  
O modelo de objeto do InfoPath também fornece um conjunto de classes de conexão de dados, contendo informações sobre as conexões de dados usado pelo formulário.
  
> [!NOTE]
> No Microsoft InfoPath 2003, uma conexão de dados é conhecida como um adaptador de dados. 
  
Conexões de dados são de dois tipos: conexões de consulta são usados para obter os dados que será então armazenados em uma fonte de dados secundário. Envie conexões são usados para enviar dados, um banco de dados ou serviço Web, por exemplo. Os dados enviados são copiados de fontes de dados principal ou secundário. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Visão geral da classe DataSourceCollection

A classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) fornece as seguintes propriedades e métodos que os desenvolvedores de formulário podem usar para gerenciar as instâncias do objeto [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) que contém o formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Retorna uma contagem do número de instâncias do objeto **DataSource** contido na coleção.  <br/> |
|Método [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx)  <br/> |Retorna um **IEnumerator** que pode ser usado para iterar na coleção.  <br/> |
|Propriedade [item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Retorna uma referência ao objeto de **fonte de dados** especificado pelo valor de índice.  <br/> |
|Propriedade [item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Retorna uma referência ao objeto de **fonte de dados** especificado pelo nome.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Visão geral da classe DataSource

A classe [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) fornece o método e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma fonte de dados secundário do InfoPath a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Retorna um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para acessar e editar fonte de dados  <br/> |
|Propriedade [QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Obtém uma referência ao objeto de conexão de dados associados.  <br/> Para executar a consulta na conexão de dados e inserir os dados retornados como XML no nó XML associado ao objeto de **fonte de dados** , use o método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) do objeto de conexão de dados associados.  <br/> |
|Propriedade [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Obtém o nome do objeto **DataSource** .  <br/> |
|Propriedade [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Obtém um valor que indica se a fonte de dados está em um estado somente leitura  <br/> |
|Método [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Obtém o valor de uma propriedade nomeada para o nó XML especificado, o que deve ser um nó de **não-atributo** da fonte de dados principal.  <br/> |
|Método [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Define o valor de uma propriedade nomeada para o nó XML especificado, o que deve ser um nó de **não-atributo** da fonte de dados principal.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Visão geral das Classes de Conexão de dados

As classes para acessar as conexões de dados fornecem diferentes propriedades e métodos que recuperar e enviam dados através de conexões para fontes de dados externas; a conexão de dados que está associado um objeto **DataSource** depende do tipo de conexão de dados externos. InfoPath implementa as seguintes classes para acessar as conexões de dados. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Classe de [AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Consulta de uma fonte de dados ADO/OLEDB; limitado ao Microsoft Access e Microsoft SQL Server.  <br/> |
|Classe de [AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Envia a uma fonte de dados ADO/OLEDB; limitado ao Microsoft Access e Microsoft SQL Server.  <br/> |
|Classe de [SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Consulta de uma biblioteca de documentos ou lista do SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Submete em uma biblioteca de documentos ou lista do SharePoint.  <br/> |
|Classe de [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Se conecta a um serviço Web XML.  <br/> |
|Classe de [FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Consulta um arquivo XML.  <br/> |
|Classe de [FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Envia para um arquivo XML.  <br/> |
|Classe de [EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Envia um formulário como um anexo de email.  <br/> |
|Classe de [BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Consulta uma lista externa em um servidor executando o SharePoint Foundation 2010 ou o SharePoint Server 2010.  <br/> |
|Classe de [BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Envia a uma lista externa em um servidor executando o SharePoint Foundation 2010 ou o SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Usando o DataSourceCollection e as Classes de fonte de dados

O objeto **DataSourceCollection** que representa a coleção de fontes de dados associados a um modelo de formulário é acessado por meio da propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Por exemplo, se você criar uma fonte de dados secundária denominada Employees que recupera os dados da tabela Employees no banco de dados Northwind, você pode usar o objeto **DataSourceCollection** para definir uma referência a um objeto de **fonte de dados** que representa a dados recuperados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundário é passado para a propriedade acessador da classe **DataSourceCollection** , que retorna uma referência ao objeto de **fonte de dados** que representa os dados recuperados da tabela Funcionários. O nó XML que armazena os dados recuperados da fonte de dados secundário é exibido em uma caixa de mensagem usando o método **CreateNavigator** da classe **DataSource** para acessar a propriedade **InnerXml** da classe **XPathNavigator** . 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

Para manipular os dados contidos em uma fonte de dados secundário, use o método **CreateNavigator** da classe **DataSource** para retornar uma referência a um objeto **XPathNavigator** posicionado no nó onde os dados do secundário estão armazenados. Você pode usar as propriedades ou métodos da classe **XPathNavigator** para manipular os dados. Para obter mais informações, consulte [trabalhar com o XPathNavigator e Classes de XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Usando o DataConnectionCollection e as Classes de DataConnection

O objeto [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) que representa a coleção de conexões de dados associados a um modelo de formulário é acessado por meio da propriedade de [conexões de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) da classe **XmlForm** . Por exemplo, se você criar uma fonte de dados secundária denominada Employees que recupera os dados da tabela Employees no banco de dados Northwind, você pode usar o objeto **DataConnectionCollection** associado ao modelo de formulário para definir uma referência para a ** DataConnection** que representa a conexão ao banco de dados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundário é passado para a propriedade acessador da classe **DataConnectionCollection** , que, nesse caso, retorna uma referência ao objeto **ADOQueryConnection** que representa o conexão ao banco de dados Northwind. Para que isso funcione corretamente, você deve converter explicitamente o objeto que está sendo retornado para o tipo de **ADOQueryConnection** . A propriedade de [Conexão](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) da interface **ADOAdapterObject** é usada para exibir a cadeia de caracteres de conexão ADO em uma caixa de mensagem. 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>Confira também



[Criando modelos de formulário do InfoPath que funcionam com o InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

