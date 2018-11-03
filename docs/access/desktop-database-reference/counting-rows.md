---
title: Contando linhas (referência de banco de dados da área de trabalho do Access)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39468086e7c78a89b13b6021c7f07853c487c6e5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945303"
---
# <a name="counting-rows"></a>Contando linhas


**Aplica-se a**: Access 2013, o Office 2013

A propriedade **RecordCount** retorna um valor **Long** que indica o número de registros no **Recordset**. Use a propriedade **RecordCount** para descobrir quantos registros existem em um objeto **Recordset**. A propriedade retorna -1 quando o ADO não pode determinar o número de registros ou se o tipo de cursor ou provedor não oferecer suporte à propriedade **RecordCount**. Ler a propriedade **RecordCount** em um objeto **Recordset** fechado produz um erro.

A propriedade **RecordCount** depende dos recursos do provedor e do tipo de cursor. A propriedade **RecordCount** retornará -1 para um cursor apenas de avanço, a contagem real para um cursor estático ou de conjunto de chaves e -1 ou a contagem real para um cursor dinâmico, dependendo da fonte de dados.

O exemplo de **Recordset** introduzidas no [Examinando dados](chapter-3-examining-data.md) retornaria – 1 porque um cursor somente de encaminhamento foi aberto. Para usar a propriedade **RecordCount**, você precisaria abrir o **Recordset** com um cursor mais sofisticado (estático ou de conjunto de chaves).

Em alguns casos, o provedor ou o cursor talvez não seja capaz de fornecer o valor **RecordCount** sem primeiro buscar todos os registros na fonte de dados. Para forçar esse tipo de busca, chame o método **MoveLast** do objeto **Recordset** antes de chamar **RecordCount**.

Se você estivava para substituir a linha de código que chama o método **Open** do objeto **Recordset** por:

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

você poderia usar a propriedade **RecordCount** porque os cursores estáticos com [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) oferecem suporte à propriedade **RecordCount**. Por exemplo, o código a seguir imprimiria o número de registros retornados pelo comando para a janela de depuração, assumindo que o cursor oferecesse suporte à propriedade **RecordCount**:

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

Deste ponto em diante, considere que essas configurações de tipo de bloqueio e cursor com mais recursos (mas mais caras) são usadas.

