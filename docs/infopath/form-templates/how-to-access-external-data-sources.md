---
title: Acessar fontes de dados externas
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- classes de conexão de dados [InfoPath 2007], fontes de dados secundárias [InfoPath 2007], dados [InfoPath 2007], secundário, classe DataSource [InfoPath 2007], acesso a fontes de dados externas [InfoPath 2007], classe dataSourcecollection [InfoPath 2007], Classe dataConnectioncollection [InfoPath 2007], classe dataConnection [InfoPath 2007], InfoPath 2007, acesso a dados externos, dados [InfoPath 2007], fontes externas
localization_priority: Normal
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar as fontes de dados secundárias do formulário e manipular os dados que elas contêm.
ms.openlocfilehash: f6957c561231eef0e3e4df6deb09ae89f85afcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408310"
---
# <a name="access-external-data-sources"></a>Acessar fontes de dados externas

Ao trabalhar com um modelo de formulário do InfoPath, você pode escrever código para acessar as fontes de dados secundárias do formulário e manipular os dados que elas contêm. 
  
Cada fonte de dados secundária é representada por um objeto instanciado usando a classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) e corresponde a dados armazenados, obtidos de algumas fontes de dados externas, como um banco de dados ou uma consulta de serviço Web. Essas fontes de dados são chamadas de secundário porque, quando o usuário salva um formulário do InfoPath, o usuário está salvando os dados somente na fonte de dados principal (ou principal), e não nos dados das fontes de dados secundárias. A conexão com uma fonte de dados é representada por um objeto instanciado usando uma das classes "conexão de dados", como a classe [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) , que representa uma conexão de dados com um serviço Web XML. 
  
O objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) instanciado representa o armazenamento de dados XML retornados por uma conexão de dados (de uma consulta de serviço Web ou de banco de dados) e a classe "conexão de dados" representa a própria conexão de dados (conforme definido e nomeado usando os **dados Comando conexões** na guia **dados** ). 
  
O modelo de objeto do InfoPath oferece suporte ao acesso a fontes de dados secundárias de um formulário por meio do uso da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) em associação com a classe DataSourceCollection. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
O modelo de objeto do InfoPath também fornece um conjunto de classes de conexão de dados, contendo informações sobre as conexões de dados usadas pelo formulário.
  
> [!NOTE]
> No Microsoft InfoPath 2003, uma conexão de dados é chamada de adaptador de dados. 
  
As conexões de dados são de dois tipos: as conexões de consulta são usadas para obter os dados que são armazenados em uma fonte de dados secundária. As conexões de envio são usadas para enviar dados para um banco de dados ou serviço Web, por exemplo. Os dados enviados são copiados das fontes de dados principais ou secundárias. 
  
## <a name="overview-of-the-datasourcecollection-class"></a>Visão geral da classe dataSourcecollection

A [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) classe DataSourceCollection fornece as seguintes propriedades e métodos, que os desenvolvedores de formulários podem usar para gerenciar as instâncias de objeto DataSourceCollection que o formulário contém. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx)  <br/> |Retorna uma contagem do número de instâncias do objeto **DataSource** contido na coleção.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) Método GetEnumerator  <br/> |Retorna um **IEnumerator** que pode ser usado para percorrer a coleção.  <br/> |
|Propriedade [Item [Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Retorna uma referência ao objeto **DataSource** especificado pelo valor de índice.  <br/> |
|Propriedade [Item [String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx)  <br/> |Retorna uma referência ao objeto **DataSource** especificado pelo nome.  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>Visão geral da classe DataSource

A [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) classe DataSourceCollection fornece o método e as propriedades a seguir, que os desenvolvedores de formulários podem usar para interagir com uma fonte de dados secundária do InfoPath. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |Retorna um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para acessar e editar a fonte de dados  <br/> |
|Propriedade [QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx)  <br/> |Obtém uma referência ao objeto de conexão de dados associado.  <br/> Para executar a consulta na conexão de dados e inserir os dados retornados como XML no nó XML associado ao objeto **DataSource** , use o método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) do objeto Connection de dados associado.  <br/> |
|Propriedade [Nome](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx)  <br/> |Obtém o nome do objeto **DataSource** .  <br/> |
|Propriedade [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx)  <br/> |Obtém um valor que indica se a fonte de dados está em um estado somente leitura  <br/> |
|Método [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |Obtém o valor de uma propriedade nomeada para o nó XML especificado, que deve ser um nó de não **atributo** na fonte de dados principal.  <br/> |
|Método [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |Define o valor de uma propriedade nomeada para o nó XML especificado, que deve ser um nó de não- **atributo** na fonte de dados principal.  <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>Visão geral das classes de conexão de dados

As classes para acessar conexões de dados fornecem propriedades e métodos diferentes que recuperam e enviam dados por meio de conexões com fontes de dados externas; a conexão de dados associada a um objeto **DataSource** depende do tipo de conexão de dados externos. O InfoPath implementa as seguintes classes para acessar conexões de dados. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Classe [AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx)  <br/> |Consulta uma fonte de dados ADO/OLEDB; limitado ao Microsoft Access e ao Microsoft SQL Server.  <br/> |
|Classe [AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx)  <br/> |Envia para uma fonte de dados ADO/OLEDB; limitado ao Microsoft Access e ao Microsoft SQL Server.  <br/> |
|Classe [SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx)  <br/> |Consulta uma lista ou biblioteca de documentos do SharePoint.  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |Envia para uma lista ou biblioteca de documentos do SharePoint.  <br/> |
|Classe [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx)  <br/> |Conecta-se a um serviço Web XML.  <br/> |
|Classe [FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx)  <br/> |Consulta um arquivo XML.  <br/> |
|Classe [FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx)  <br/> |Envia para um arquivo XML.  <br/> |
|Classe [EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx)  <br/> |Envia um formulário como um anexo no email.  <br/> |
|Classe [BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx)  <br/> |Consulta uma lista externa em um servidor que executa o SharePoint Foundation 2010 ou o SharePoint Server 2010.  <br/> |
|Classe [BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx)  <br/> |Envia para uma lista externa em um servidor que executa o SharePoint Foundation 2010 ou o SharePoint Server 2010.  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>Usando as classes dataSourcecollection e DataSource

O **** objeto DataSourceCollection que representa a coleção de fontes de dados associada a um modelo de formulário é acessado por meio da Propriedade DataSources da classe [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) XmlForm. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera os dados da tabela Employees no banco de dados Northwind, **** você poderá usar o objeto DataSourceCollection para definir uma referência a um objeto **DataSource** que representa o dados recuperados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade acessador da classe dataSourcecollection, que retorna uma referência ao objeto **DataSource** que representa os dados da tabela Employees recuperados. **** O nó XML que armazena os dados recuperados da fonte de dados secundária é exibido em uma caixa de mensagem **** usando o método CreateNavigator da classe **DataSource** para acessar a propriedade **InnerXml** da classe **XPathNavigator** . 
  
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

Para manipular os dados que estão contidos em uma fonte de dados secundária, use **** o método CreateNavigator da classe **DataSource** para retornar uma referência a um objeto **XPathNavigator** posicionado no nó em que os dados secundários estão armazenados. Você pode usar as propriedades ou métodos da classe **XPathNavigator** para manipular os dados. Para obter mais informações, consulte [trabalhar com as classes XPathNavigator e XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>Usando as classes dataConnectcollection e dataConnection

O [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) objeto dataconnectcollection que representa a coleção de conexões de dados associada a um modelo de formulário é acessado por meio da propriedade DataConnections da classe [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) XmlForm. **** Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera os dados da tabela Employees no banco de dados Northwind, **** poderá usar o objeto dataconnectcollection associado ao modelo de formulário para definir uma referência ao ** **DataConnection que representa a conexão com o banco de dados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade acessador da classe dataConnectioncollection, que, nesse caso, retorna uma referência ao objeto **ADOQueryConnection** que representa o **** conexão com o banco de dados Northwind. Para que isso funcione corretamente, você deve converter explicitamente o objeto que está sendo retornado para o tipo **ADOQueryConnection** . A propriedade [Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) da interface **ADOAdapterObject** é usada para exibir a cadeia de caracteres de conexão ADO em uma caixa de mensagem. 
  
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



[Criar modelos de formulário do InfoPath que funcionam com o InfoPath Forms Services](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

