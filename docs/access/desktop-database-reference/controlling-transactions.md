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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716618"
---
# <a name="controlling-transactions"></a><span data-ttu-id="672e1-102">Controlando transações</span><span class="sxs-lookup"><span data-stu-id="672e1-102">Controlling Transactions</span></span>


<span data-ttu-id="672e1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="672e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="672e1-104">Uma *transação* delimita início e no final de uma série de operações de acesso de dados que se passar através de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="672e1-104">A *transaction* delimits the beginning and end of a series of data access operations that transpire across a connection.</span></span> <span data-ttu-id="672e1-105">De acordo com os recursos transacionais da fonte de dados, o objeto **Connection** também permite criar e gerenciar transações.</span><span class="sxs-lookup"><span data-stu-id="672e1-105">Subject to the transactional capabilities of your data source, the **Connection** object also allows you to create and manage transactions.</span></span> <span data-ttu-id="672e1-106">Por exemplo, usando o Microsoft OLE DB Provider for SQL Server para acessar um banco de dados no Microsoft SQL Server 2000, é possível criar várias transações aninhadas para os comandos que você executar.</span><span class="sxs-lookup"><span data-stu-id="672e1-106">For example, using the Microsoft OLE DB Provider for SQL Server to access a database on Microsoft SQL Server 2000, you can create multiple nested transactions for the commands you execute.</span></span>

<span data-ttu-id="672e1-107">O ADO garante que as alterações de uma fonte de dados, resultantes das operações de uma transação, ou são todas bem-sucedidas, ou nenhuma é realizada.</span><span class="sxs-lookup"><span data-stu-id="672e1-107">ADO ensures that changes to a data source resulting from operations in a transaction occur successfully together or not at all.</span></span>

<span data-ttu-id="672e1-p102">Se você cancelar a transação ou se uma das suas operações falhar, o resultado final será como se nenhuma das operações da transação tivesse ocorrido. A fonte de dados continuará sendo a mesma de antes do início da transação.</span><span class="sxs-lookup"><span data-stu-id="672e1-p102">If you cancel the transaction, or if one of its operations fails, the ultimate result will be as if none of the operations in the transaction occurred. The data source will remain as it was before the transaction began.</span></span>

<span data-ttu-id="672e1-110">O modelo de objeto do ADO não inclui as transações de maneira explícita, mas as representa com um conjunto de métodos do objeto **Connection** (**BeginTrans**, **CommitTrans** e **RollbackTrans**).</span><span class="sxs-lookup"><span data-stu-id="672e1-110">The ADO object model does not explicitly include transactions, but represents them with a set of **Connection** object methods (**BeginTrans**, **CommitTrans**, and **RollbackTrans**).</span></span>

<span data-ttu-id="672e1-111">Para obter mais informações sobre transações, consulte [Capítulo 5: Atualizando e mantendo dados](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="672e1-111">For more information about transactions, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

