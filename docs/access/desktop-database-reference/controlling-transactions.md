---
title: Controlando transações
TOCTitle: Controlling Transactions
ms:assetid: 21a9f055-6907-3818-e232-21e579cc67b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248994(v=office.15)
ms:contentKeyID: 48543685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ced1ae7b32d25fbae53c670959a4a6c77bcea0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295545"
---
# <a name="controlling-transactions"></a>Controlando transações


**Aplica-se ao:** Access 2013, Office 2013

Uma *transação* delimita o início e o fim de uma série de operações de acesso a dados que ocorrem em uma conexão. De acordo com os recursos transacionais da fonte de dados, o objeto **Connection** também permite criar e gerenciar transações. Por exemplo, usando o Microsoft OLE DB Provider for SQL Server para acessar um banco de dados no Microsoft SQL Server 2000, é possível criar várias transações aninhadas para os comandos que você executar.

O ADO garante que as alterações de uma fonte de dados, resultantes das operações de uma transação, ou são todas bem-sucedidas, ou nenhuma é realizada.

Se você cancelar a transação ou se uma das suas operações falhar, o resultado final será como se nenhuma das operações da transação tivesse ocorrido. A fonte de dados continuará sendo a mesma de antes do início da transação.

O modelo de objeto do ADO não inclui as transações de maneira explícita, mas as representa com um conjunto de métodos do objeto **Connection** (**BeginTrans**, **CommitTrans** e **RollbackTrans**).

Para obter mais informações sobre transações, consulte [Capítulo 5: Atualizando e mantendo dados](chapter-5-updating-and-persisting-data.md).

