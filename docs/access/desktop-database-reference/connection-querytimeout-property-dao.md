---
title: Propriedade Connection.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 51f2f51743a8f92b77fafacebbc18e11eb77fe8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462665"
---
# <a name="connectionquerytimeout-property-dao"></a>Propriedade Connection.QueryTimeout (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . QueryTimeout

*expressão* Uma variável que representa um objeto de **Conexão** .

## <a name="remarks"></a>Comentários

O valor padrão é 60.

Quando você está utilizando um banco de dados ODBC, como o Microsoft SQL Server, pode haver atrasos devido ao tráfego da rede ou ao uso pesado do servidor ODBC. Em vez aguardar por um tempo indefinido, você poderá especificar o tempo de espera.

Quando você usar **QueryTimeout** com um objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, essa propriedade especificará um valor global para todas as consultas associadas ao banco de dados. É possível substituir esse valor para uma consulta específica pela definição da propriedade **ODBCTimeout** de um objeto **[QueryDef](querydef-object-dao.md)** específico.

