---
title: Método Query (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a9ecb2d7ebfdd8f6738b8d7b9b8738ce981ec16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462432"
---
# <a name="query-method-rds"></a>Método Query (RDS)


**Aplica-se a**: Access 2013 | Office 2013


Utiliza uma sequência de consulta SQL válida para retornar um [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

Definir o*Recordset* = *DataFactory*. Consulta (*Conexão*, *consulta*)

## <a name="parameters"></a>Parâmetros

  - *Recordset*

  - Uma variável de objeto que representa um objeto **Recordset**.

  - *DataFactory*

  - Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).

  - *Connection*

  - Um valor **String** que contém as informações de conexão do servidor. Isso é semelhante à propriedade [Connect](connect-property-rds.md).

  - *Query*

  - Uma **String** que contém a consulta SQL.

## <a name="remarks"></a>Comentários

A consulta deve utilizar o dialeto SQL do servidor de banco de dados. Um status de resultado será retornado se houver um erro com a consulta que foi executada. O método **Query** não desempenha nenhuma verificação de sintaxe na sequência **Query**.

