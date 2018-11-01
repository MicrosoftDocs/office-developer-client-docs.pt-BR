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
# <a name="required-providers-for-data-shaping"></a>Provedores necessários para o data shaping


**Aplica-se a**: Access 2013, o Office 2013

O data shaping geralmente requer dois provedores. O provedor de serviços, [Serviço de data shaping para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fornece a funcionalidade de data shaping, e um provedor de dados, como o OLE DB Provider for SQL Server, fornece linhas de dados para preenchimento do [Recordset](recordset-object-ado.md) com formato.

O nome do provedor de serviços (MSDataShape) pode ser especificado como o valor da propriedade [Provider](connection-object-ado.md) do objeto [Connection](provider-property-ado.md) ou a palavra-chave "Provider=MSDataShape;" da sequência de conexão.

O nome do provedor de dados pode ser especificado como o valor da propriedade dinâmica **Provedor de dados** , que é adicionado à coleção [Properties](properties-collection-ado.md) do objeto de **Conexão** pelo Data Shaping Service para OLE DB ou a palavra-chave cadeia de caracteres de conexão "* *Provedor de dados = * * * provedor*".

Nenhum provedor de dados será necessário se **Recordset** não estiver preenchido (por exemplo, como em um **Recordset** fabricado, em que as colunas são criadas com a palavra-chave NEW). Nesse caso, especifique "**Data Provider=** none;".

## <a name="example"></a>Exemplo

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

