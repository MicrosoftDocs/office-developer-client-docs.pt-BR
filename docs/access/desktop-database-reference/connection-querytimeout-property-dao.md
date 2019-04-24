---
title: Propriedade Connection. QueryTimeout (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295818"
---
# <a name="connectionquerytimeout-property-dao"></a>Propriedade Connection. QueryTimeout (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . QueryTimeout

*expressão* Uma variável que representa um objeto **Connection** .

## <a name="remarks"></a>Comentários

O valor padrão é 60.

Quando você está utilizando um banco de dados ODBC, como o Microsoft SQL Server, pode haver atrasos devido ao tráfego da rede ou ao uso pesado do servidor ODBC. Em vez aguardar por um tempo indefinido, você poderá especificar o tempo de espera.

Quando você usar **QueryTimeout** com um objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, essa propriedade especificará um valor global para todas as consultas associadas ao banco de dados. É possível substituir esse valor para uma consulta específica pela definição da propriedade **ODBCTimeout** de um objeto **[QueryDef](querydef-object-dao.md)** específico.

