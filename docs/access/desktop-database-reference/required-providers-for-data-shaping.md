---
title: Provedores necessários para Data Shaping
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306654"
---
# <a name="required-providers-for-data-shaping"></a>Provedores necessários para Data Shaping

**Aplica-se ao:** Access 2013, Office 2013

O data shaping geralmente requer dois provedores. O provedor de serviços, [Serviço de data shaping para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), fornece a funcionalidade de data shaping, e um provedor de dados, como o OLE DB Provider for SQL Server, fornece linhas de dados para preenchimento do [Recordset](recordset-object-ado.md) com formato.

O nome do provedor de serviços (MSDataShape) pode ser especificado como o valor da propriedade [Provider](connection-object-ado.md) do objeto [Connection](provider-property-ado.md) ou a palavra-chave "Provider=MSDataShape;" da sequência de conexão.

O nome do provedor de dados pode ser especificado como o valor da propriedade dinâmica do **provedor de dados** , que é adicionado à coleção [Properties](properties-collection-ado.md) do objeto **Connection** pelo serviço de data Shaping para OLE DB ou a palavra-chave de sequência de conexão "* *Provedor de dados = * * * provedor*".

Nenhum provedor de dados será necessário se **Recordset** não estiver preenchido (por exemplo, como em um **Recordset** fabricado, em que as colunas são criadas com a palavra-chave NEW). Nesse caso, especifique "**Data Provider=** none;".

## <a name="example"></a>Exemplo

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

