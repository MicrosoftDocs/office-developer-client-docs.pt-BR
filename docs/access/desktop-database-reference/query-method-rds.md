---
title: Método Query (RDS - referência do banco de dados da área de trabalho do Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301110"
---
# <a name="query-method-rds"></a>Método Query (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Utiliza uma sequência de consulta SQL válida para retornar um [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

Definir *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Recordset* |Uma variável de objeto que representa um objeto **Recordset**.|
|*DataFactory* |Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connection* |Um valor **String** que contém as informações de conexão do servidor. Isso é semelhante à propriedade [Connect](connect-property-rds.md).|
|*Query* |Uma **String** que contém a consulta SQL.|

## <a name="remarks"></a>Comentários

A consulta deve utilizar o dialeto SQL do servidor de banco de dados. Um status de resultado será retornado se houver um erro com a consulta que foi executada. O método **Query** não desempenha nenhuma verificação de sintaxe na sequência **Query**.

