---
title: Acessar fontes de dados externas usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- fontes de dados [infopath 2007], acessando com o modelo de objeto do infopath 2003, modelos de formulário compatíveis com InfoPath 2003, acessando dados externos
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
  
Cada fonte de dados secundária é representada por um objeto instanado usando a interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) e corresponde aos dados armazenados, obtidos de alguma fonte externa de dados, como um banco de dados ou uma consulta de Serviço Web. Essas fontes de dados são conhecidas como secundárias porque, quando o usuário salva um formulário do InfoPath, o usuário está salvando os dados apenas na fonte de dados principal, não os dados nas fontes de dados secundárias. A conexão com uma fonte de dados é representada por um objeto instando usando uma das interfaces "adaptador de dados", como a interface [WebServiceAdapterObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) que representa uma conexão de dados com um Serviço Web XML. 
  
O objeto [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) instaliado representa o armazenamento de dados XML retornados por uma conexão de dados (para um banco de dados ou consulta de Serviço Web), e o adaptador de dados representa a própria conexão de dados. 
  
O modelo de objeto do InfoPath dá suporte ao acesso a fontes de dados secundárias de um formulário por meio do uso da interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) em associação com a interface [DataObjectsCollection.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) 
  
O modelo de objeto do InfoPath também fornece um conjunto de objetos de adaptador de dados, contendo informações sobre as conexões de dados usadas pelo formulário. 
  
Há dois tipos de adaptadores de dados: adaptadores de consulta e adaptadores Enviar. Os adaptadores de consulta são usados para obter os dados armazenados em uma fonte de dados secundária, enquanto os adaptadores Enviar são usados para enviar dados para um banco de dados ou serviço Web, por exemplo. Os dados enviados são copiados das fontes de dados principais ou secundárias. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Visão geral da interface DataObjectsCollection

A interface [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) fornece as seguintes propriedades e métodos, que os desenvolvedores de formulário podem usar para gerenciar as instâncias [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) que o formulário contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Retorna uma contagem do número de **instâncias DataSourceObject** contidas na coleção.  <br/> |
|[Método GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Retorna um **IEnumerator** que pode ser usado para iterar através da coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Retorna uma referência à instância **DataSourceObject** especificada.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Visão geral da interface DataSourceObject

A interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) fornece o método e as propriedades a seguir, que os desenvolvedores de formulário podem usar para interagir com uma fonte de dados secundária do InfoPath. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[Método Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Executa a consulta no adaptador de dados e insere os dados retornados como XML no DOM (Modelo de Objeto de Documento XML) associado ao **DataSourceObject**.  <br/> |
|[Propriedade DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML usado para armazenar e manipular dados usando **DataSourceObject**.  <br/> |
|Propriedade [Nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Retorna um valor de cadeia de caracteres indicando o nome do **DataSourceObject**.  <br/> |
|[Propriedade QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto do adaptador de dados associado.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Visão geral das Interfaces do Adaptador de Dados

As interfaces para acessar adaptadores de dados fornecem diferentes propriedades e métodos que recuperam e enviam dados por meio de conexões a fontes de dados externas; o adaptador de dados associado a um [objeto DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) depende do tipo de conexão de dados externa. O InfoPath implementa as interfaces a seguir para acessar adaptadores de dados. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Interface [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Conecta-se a fontes de dados do ADO/OLEDB; limitado ao Microsoft Access e ao Microsoft SQL Server™.  <br/> |
|Interface [SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Conecta-se a uma lista ou biblioteca de documentos do SharePoint.  <br/> |
|Interface [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Conecta-se aos serviços Web XML.  <br/> |
|[Objeto XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Conecta-se a um arquivo XML.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Usando o DataSourceObjects e as interfaces DataSourceObject

A **coleção DataSourceObjects** é acessada por meio da propriedade [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) da interface [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera dados da tabela Employees no banco de dados northwind Traders microsoft Access, você pode usar a coleção **DataSourceObjects** para definir uma referência a um objeto **DataObject** que representa os dados recuperados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade de acesso da interface **DataObjectsCollection,** que retorna uma referência ao objeto **DataSourceObject** . Os dados da fonte de dados secundária são exibidos em uma caixa de mensagem usando a propriedade **DOM** da interface **DataSourceObject** para acessar a propriedade **xml** do DOM XML. 
  
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

Para manipular os dados contidos em uma fonte de dados secundária, use a propriedade **DOM** da interface **DataSourceObject** para retornar uma referência ao DOM XML que contém os dados. Quando você tiver a referência ao DOM XML, poderá usar qualquer uma de suas propriedades ou métodos para manipular os dados que ele contém. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Usando as interfaces DataAdaptersCollection e DataAdapterObject

A interface [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) é acessada por meio da [propriedade DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) da interface **XDocument.** Por exemplo, se você criar uma fonte de dados secundária chamada Employees que recupera dados da tabela Employees no banco de dados northwind Traders microsoft Access, você pode usar a coleção **DataAdapterObjects** para definir uma referência ao **DataAdapterObject** que representa a conexão com o banco de dados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundária é passado para a propriedade de acesso do **DataAdaptersCollection**, que, nesse caso, retorna uma referência a uma instância do **ADOAdapterObject** que representa a conexão com o banco de dados northwind do Microsoft Access. Para que isso funcione corretamente, você deve lançar explicitamente o objeto que está sendo retornado como um **ADOAdapterObject**. A [propriedade Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) da interface **ADOAdapterObject** é usada para exibir a sequência de conexão do ADO em uma caixa de mensagem. 
  
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


