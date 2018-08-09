---
title: Acessar fontes de dados externas usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Acessando fontes de dados [infopath 2007], com o modelo de objeto do infopath 2003, modelos de formulário compatíveis com o InfoPath 2003, como acessar dados externos
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: Ao trabalhar com um modelo de formulário do InfoPath que utiliza o modelo de objeto compatível do InfoPath 2003, você pode escrever código para acessar fontes de dados secundária do formulário e manipular os dados que elas contêm.
ms.openlocfilehash: cf06cdc6a02eba855442cdab4c3c698ed3f4425f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765601"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>Acessar fontes de dados externas usando o modelo de objeto do InfoPath 2003

Ao trabalhar com um modelo de formulário do InfoPath que utiliza o modelo de objeto compatível do InfoPath 2003, você pode escrever código para acessar fontes de dados secundária do formulário e manipular os dados que elas contêm.
  
Cada fonte de dados secundário é representado por um objeto instanciado usando a interface [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) e corresponde aos dados armazenados, obtidos de alguma origem externa de dados, como um banco de dados ou uma consulta de serviço Web. Essas fontes de dados são referidas como secundário porque quando o usuário salvar um formulário do InfoPath, o usuário está salvando os dados somente na fonte de dados principal, e não os dados nas fontes de dados secundário. A conexão a uma fonte de dados é representado por um objeto instanciado usando uma das interfaces "adaptador de dados", como a interface de [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) , que representa uma conexão de dados para um serviço Web XML. 
  
O objeto de [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) instanciado representa o armazenamento de dados XML retornados por uma conexão de dados (para um banco de dados ou uma consulta de serviço da Web) e o adaptador de dados representa a conexão de dados em si. 
  
O modelo de objeto do InfoPath suporta acesso a fontes de dados secundário de um formulário com o uso da interface de [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) em associação com a interface [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) . 
  
O modelo de objeto do InfoPath também fornece um conjunto de objetos do adaptador de dados, contendo informações sobre as conexões de dados usado pelo formulário. 
  
Existem dois tipos de adaptadores de dados: adaptadores de consulta e enviar adaptadores. Adaptadores de consulta são usados para obter os dados que será então armazenados em uma fonte de dados secundário enquanto adaptadores de envio são usados para enviar dados, um banco de dados ou serviço Web, por exemplo. Os dados enviados são copiados de fontes de dados principal ou secundário. 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>Visão geral da Interface DataObjectsCollection

A interface de [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) oferece as seguintes propriedades e métodos que os desenvolvedores de formulário podem usar para gerenciar as instâncias de [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) que contém o formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx)  <br/> |Retorna uma contagem do número de instâncias de **DataSourceObject** contido na coleção.  <br/> |
|Método [GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx)  <br/> |Retorna um **IEnumerator** que pode ser usado para iterar na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx)  <br/> |Retorna uma referência à instância **DataSourceObject** especificada.  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>Visão geral da Interface DataSourceObject

A interface de [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) oferece o seguinte método e propriedades, que os desenvolvedores de formulário podem usar para interagir com uma fonte de dados secundário do InfoPath. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx)  <br/> |Executa a consulta no adaptador de dados e insere os dados retornados como XML para o XML DOM Document Object Model () associados com o **DataSourceObject**.  <br/> |
|Propriedade [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx)  <br/> |Retorna uma referência ao DOM XML usado para armazenar e manipular dados usando o **DataSourceObject**.  <br/> |
|Propriedade [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx)  <br/> |Retorna um valor de cadeia de caracteres indicando o nome da **DataSourceObject**.  <br/> |
|Propriedade [QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx)  <br/> |Retorna uma referência ao objeto adaptador de dados associados.  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>Visão geral das Interfaces do adaptador de dados

As interfaces para acessar os adaptadores de dados fornecem diferentes propriedades e métodos que recuperar e enviam dados através de conexões para fontes de dados externas; adaptador de dados que é associado a um objeto [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) depende do tipo de conexão de dados externos. InfoPath implementa as seguintes interfaces para acessar os adaptadores de dados. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Interface de [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx)  <br/> |Conecta-se às fontes de dados ADO/OLEDB; limitado ao Microsoft Access e Microsoft SQL Server™.  <br/> |
|Interface de [SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx)  <br/> |Conecta-se em uma biblioteca de documentos ou lista do SharePoint.  <br/> |
|Interface de [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx)  <br/> |Conecta-se aos serviços Web XML.  <br/> |
|Objeto [XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx)  <br/> |Conecta-se para um arquivo XML.  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>Usando o DataSourceObjects e as Interfaces de DataSourceObject

A coleção de **DataSourceObjects** é acessada por meio da propriedade [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Por exemplo, se você criar uma fonte de dados secundária denominada Employees que recupera os dados da tabela Employees no banco de dados Northwind Traders Microsoft Access, você pode usar a coleção **DataSourceObjects** para definir uma referência para um **DataObject** objeto que representa os dados recuperados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundário é passado para a propriedade acessador da interface **DataObjectsCollection** , que retorna uma referência ao objeto **DataSourceObject** . Os dados da fonte de dados secundário são exibidos em uma caixa de mensagem usando a propriedade **DOM** da interface **DataSourceObject** para acessar a propriedade **xml** do DOM. XML 
  
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

Para manipular os dados contidos em uma fonte de dados secundário, use a propriedade **DOM** da interface **DataSourceObject** para retornar uma referência ao DOM XML que contém os dados. Quando você tem a referência ao DOM XML, você pode usar qualquer uma das suas propriedades ou métodos para manipular os dados que ele contém. 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>Usando o DataAdaptersCollection e as Interfaces de DataAdapterObject

A interface [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) é acessada por meio da propriedade [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) da interface **XDocument** . Por exemplo, se você criar uma fonte de dados secundária denominada Employees que recupera os dados da tabela Employees no banco de dados Northwind Traders Microsoft Access, você pode usar a coleção **DataAdapterObjects** para definir uma referência para a ** DataAdapterObject** que representa a conexão ao banco de dados. 
  
No exemplo de código a seguir, o nome da fonte de dados secundário é passado para a propriedade de acessador do **DataAdaptersCollection**, que, nesse caso, retorna uma referência a uma instância de **ADOAdapterObject** que representa a conexão no banco de dados Northwind do Microsoft Access. Para que isso funcione corretamente, você deve converter explicitamente o objeto que está sendo retornado como um **ADOAdapterObject**. A propriedade de [Conexão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) da interface **ADOAdapterObject** é usada para exibir a cadeia de caracteres de conexão ADO em uma caixa de mensagem. 
  
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


