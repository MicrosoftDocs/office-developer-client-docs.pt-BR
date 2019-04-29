---
title: Acessar fontes de dados externas usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- fontes de dados [InfoPath 2007], acessando com o modelo de objeto do InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, acessar dados externos
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Ao trabalhar com um modelo de formulário do InfoPath que usa o modelo de objeto compatível com o InfoPath 2003, você pode escrever código para acessar as fontes de dados secundárias do formulário e manipular os dados que elas contêm.
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431677"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Acessar fontes de dados externas usando o modelo de objeto do InfoPath 2003

Ao trabalhar com um modelo de formulário do InfoPath que usa o modelo de objeto compatível com o InfoPath 2003, você pode escrever código para acessar as fontes de dados secundárias do formulário e manipular os dados que elas contêm.
  
Cada fonte de dados secundária é representada por um objeto instanciado usando [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) a interface DataSourceObject e corresponde a dados armazenados, obtidos de algumas fontes de dados externas, como um banco de dados ou uma consulta de serviço Web. Essas fontes de dados são chamadas de secundário porque, quando o usuário salva um formulário do InfoPath, o usuário está salvando os dados apenas na fonte de dados principal, e não nos dados das fontes de dados secundárias. A conexão com uma fonte de dados é representada por um objeto instanciado usando uma das interfaces "adaptador de dados", como a interface [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) , que representa uma conexão de dados com um serviço Web XML. 
  
O objeto dataSourceobject instanciado representa o armazenamento de dados XML retornados por uma conexão de dados (para um banco de dados ou uma consulta de serviço Web) e o adaptador de dados representa a própria conexão de dados. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) 
  
O modelo de objeto do InfoPath oferece suporte ao acesso a fontes de dados secundárias de um [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) formulário por meio do uso da interface DataSourceObject em associação com a interface DataObjects. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) 
  
O modelo de objeto do InfoPath também fornece um conjunto de objetos adaptadores de dados, contendo informações sobre as conexões de dados usadas pelo formulário. 
  
Há dois tipos de adaptadores de dados: adaptadores de consulta e envio de adaptadores. Os adaptadores de consulta são usados para obter os dados que são armazenados em uma fonte de dados secundária, ao passo que os adaptadores de envio são usados para enviar dados para um banco de dados ou serviço Web, por exemplo. Os dados enviados são copiados das fontes de dados principais ou secundárias. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Visão geral da interface dataObjects

A [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) interface dataobjectcollection fornece as seguintes propriedades e métodos, que os desenvolvedores de formulários podem usar para gerenciar as instâncias de DataSourceObject que o formulário contém. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Retorna uma contagem do número de instâncias **** de DataSourceObject contidas na coleção.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) Método GetEnumerator  <br/> |Retorna um **IEnumerator** que pode ser usado para percorrer a coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Retorna uma referência para a instância **** DataSourceObject especificada.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Visão geral da interface dataSourceobject

A [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) interface DataSourceObject fornece o método e as propriedades a seguir, que os desenvolvedores de formulários podem usar para interagir com uma fonte de dados secundária do InfoPath. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Executa a consulta no adaptador de dados e insere os dados retornados como XML no modelo de objeto de documento XML (DOM) associado ao dataSourceobject. ****  <br/> |
|Propriedade [dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML usado para armazenar e manipular dados usando dataSourceobject. ****  <br/> |
|Propriedade [Nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Retorna um valor String que indica o nome do **** DataSourceObject.  <br/> |
|Propriedade [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto adaptador de dados associado.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Visão geral das interfaces de adaptador de dados

As interfaces para acessar adaptadores de dados fornecem propriedades e métodos diferentes que recuperam e enviam dados por meio de conexões com fontes de dados externas; o adaptador de dados associado a um objeto [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) DataSourceObject depende do tipo de conexão de dados externos. O InfoPath implementa as seguintes interfaces para acessar adaptadores de dados. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Interface [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Conecta-se às fontes de dados ADO/OLEDB; limitado ao Microsoft Access e ao Microsoft SQL Server ™.  <br/> |
|Interface [SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Conecta-se a uma lista ou biblioteca de documentos do SharePoint.  <br/> |
|Interface [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Conecta-se aos serviços XML da Web.  <br/> |
|Objeto [XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Conecta-se a um arquivo XML.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Usando as interfaces DataSourceObjects e dataSourceobject

A coleção **DataSourceObjects** é acessada por meio da propriedade DataObjects da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera os dados da tabela Employees no banco de dados do Microsoft Access da Northwind Traders, você pode usar a coleção **DataSourceObjects** para definir uma referência a um **DataObject** objeto que representa os dados recuperados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade acessador da interface dataObjects, que retorna uma referência ao objeto dataSourceobject. **** **** Os dados da fonte de dados secundária são exibidos em uma caixa de mensagem usando a propriedade **dom** da interface **** DataSourceObject para acessar a propriedade **XML** do Dom XML. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

Para manipular os dados contidos em uma fonte de dados secundária, use a propriedade **dom** da interface DataSourceObject para retornar uma referência ao Dom XML que contém os dados. **** Quando você tiver a referência ao DOM XML, poderá usar qualquer uma de suas propriedades ou métodos para manipular os dados que ele contém. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Usando as interfaces DataAdapters e dataAdapterobject

A [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) interface dataadaptercollection é acessada por meio da propriedade DataAdapters da interface **XDocument** . [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera os dados da tabela Employees no banco de dados do Microsoft Access da Northwind Traders, você pode usar a coleção **DataAdapterObjects** para definir uma referência ao ** **Dataadapterobject que representa a conexão com o banco de dados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade acessador de dataAdapters, que, nesse caso, retorna uma referência a uma instância do **ADOAdapterObject** que representa a conexão **** para o banco de dados Northwind do Microsoft Access. Para que isso funcione corretamente, você deve converter explicitamente o objeto que está sendo retornado como um **ADOAdapterObject**. A propriedade [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) da interface **ADOAdapterObject** é usada para exibir a cadeia de caracteres de conexão ADO em uma caixa de mensagem. 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


