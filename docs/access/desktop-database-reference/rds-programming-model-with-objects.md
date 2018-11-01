---
title: Modelo de programação RDS com objetos
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6d28373e5d241ae9e87357187894924f27ba78c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873800"
---
# <a name="rds-programming-model-with-objects"></a>Modelo de programação RDS com objetos


**Aplica-se a**: Access 2013, o Office 2013

A meta do RDS é obter acesso a fontes de dados e atualizá-las através de um intermediário, como o IIS. O modelo de programação especifica a sequência de atividades necessárias para atingir essa meta. O modelo de objeto especifica os objetos cujos métodos e propriedades afetam o modelo de programação.

O RDS permite executar a sequência de ações a seguir:

  - Especifique o programa a ser chamado no servidor e encontre uma maneira (proxy) de fazer referência a ele a partir do cliente ([RDS.DataSpace](dataspace-object-rds.md)).

  - Chame o programa de servidor. Passe parâmetros para o programa de servidor que identifica a fonte de dados e o comando a ser emitido (proxy ou [RDS.DataControl](datacontrol-object-rds.md)).

  - O programa de servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** será processado no servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

  - O programa de servidor retorna o objeto **Recordset** final ao aplicativo cliente (proxy).

  - No cliente, o objeto **Recordset** é colocado em um formato que pode ser facilmente usado por controles visuais (controle visual e **RDS.DataControl**).

  - As alterações feitas no objeto **Recordset** são reenviadas ao servidor e usadas para atualizar a fonte de dados (**RDS.DataControl** ou **RDSServer.DataFactory**).

