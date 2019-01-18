---
title: Propriedade Workspace.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699608"
---
# <a name="workspacelogintimeout-property-dao"></a>Propriedade Workspace.LoginTimeout (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.

## <a name="syntax"></a>Sintaxe

*expressão* . LoginTimeout

*expressão* Uma variável que representa um objeto **Workspace** .

## <a name="remarks"></a>Comentários

A definição da propriedade **LoginTimeout** padrão é de 20 segundos. Quando a propriedade **LoginTimeout** estiver definida como 0, não haverá tempo limite.

Quando você estiver tentando fazer logon em um banco de dados ODBC, como o Microsoft SQL Server, a conexão poderá falhar como resultado de erros de rede ou porque o servidor não estava em execução. Em vez de aguardar os 20 segundos padrão para se conectar, especifique quanto tempo será necessário aguardar antes da ocorrência de um erro. O logon no servidor acontece de forma implícita como parte de diversos eventos diferentes, como a execução de uma consulta em um banco de dados de servidor externo.

