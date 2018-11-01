---
title: Provedores necessários para o data shaping
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de8634503c81bd2c66eeda0c64a8b1ff1b6f5363
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885345"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="58d37-102">Provedores necessários para o data shaping</span><span class="sxs-lookup"><span data-stu-id="58d37-102">Required Providers for Data Shaping</span></span>


<span data-ttu-id="58d37-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="58d37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="58d37-p101">O data shaping geralmente requer dois provedores. O provedor de serviços, [Serviço de data shaping para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fornece a funcionalidade de data shaping, e um provedor de dados, como o OLE DB Provider for SQL Server, fornece linhas de dados para preenchimento do [Recordset](recordset-object-ado.md) com formato.</span><span class="sxs-lookup"><span data-stu-id="58d37-p101">Data shaping typically requires two providers. The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="58d37-106">O nome do provedor de serviços (MSDataShape) pode ser especificado como o valor da propriedade [Provider](connection-object-ado.md) do objeto [Connection](provider-property-ado.md) ou a palavra-chave "Provider=MSDataShape;" da sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="58d37-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="58d37-107">O nome do provedor de dados pode ser especificado como o valor da propriedade dinâmica **Provedor de dados** , que é adicionado à coleção [Properties](properties-collection-ado.md) do objeto de **Conexão** pelo Data Shaping Service para OLE DB ou a palavra-chave cadeia de caracteres de conexão "\* *Provedor de dados = \* \* \* provedor*".</span><span class="sxs-lookup"><span data-stu-id="58d37-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="58d37-p102">Nenhum provedor de dados será necessário se **Recordset** não estiver preenchido (por exemplo, como em um **Recordset** fabricado, em que as colunas são criadas com a palavra-chave NEW). Nesse caso, especifique "**Data Provider=** none;".</span><span class="sxs-lookup"><span data-stu-id="58d37-p102">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword). In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="58d37-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="58d37-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

