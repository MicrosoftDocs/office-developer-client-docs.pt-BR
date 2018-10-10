---
title: Modelo de programação RDS com objetos
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 833d3676c8fa3fac1e5cb8e16477073cde611199
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462928"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="d84e5-102">Modelo de programação RDS com objetos</span><span class="sxs-lookup"><span data-stu-id="d84e5-102">RDS Programming Model with Objects</span></span>


<span data-ttu-id="d84e5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d84e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d84e5-p101">A meta do RDS é obter acesso a fontes de dados e atualizá-las através de um intermediário, como o IIS. O modelo de programação especifica a sequência de atividades necessárias para atingir essa meta. O modelo de objeto especifica os objetos cujos métodos e propriedades afetam o modelo de programação.</span><span class="sxs-lookup"><span data-stu-id="d84e5-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="d84e5-107">O RDS permite executar a sequência de ações a seguir:</span><span class="sxs-lookup"><span data-stu-id="d84e5-107">RDS provides the means to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="d84e5-108">Especifique o programa a ser chamado no servidor e encontre uma maneira (proxy) de fazer referência a ele a partir do cliente ([RDS.DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="d84e5-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

  - <span data-ttu-id="d84e5-p102">Chame o programa de servidor. Passe parâmetros para o programa de servidor que identifica a fonte de dados e o comando a ser emitido (proxy ou [RDS.DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="d84e5-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

  - <span data-ttu-id="d84e5-p103">O programa de servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** será processado no servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="d84e5-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

  - <span data-ttu-id="d84e5-113">O programa de servidor retorna o objeto **Recordset** final ao aplicativo cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="d84e5-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

  - <span data-ttu-id="d84e5-114">No cliente, o objeto **Recordset** é colocado em um formato que pode ser facilmente usado por controles visuais (controle visual e **RDS.DataControl**).</span><span class="sxs-lookup"><span data-stu-id="d84e5-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

  - <span data-ttu-id="d84e5-115">As alterações feitas no objeto **Recordset** são reenviadas ao servidor e usadas para atualizar a fonte de dados (**RDS.DataControl** ou **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="d84e5-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

