---
title: Modelo de programação do RDS com objetos
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301047"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="876d7-102">Modelo de programação do RDS com objetos</span><span class="sxs-lookup"><span data-stu-id="876d7-102">RDS programming model with objects</span></span>

<span data-ttu-id="876d7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="876d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="876d7-p101">A meta do RDS é obter acesso a fontes de dados e atualizá-las através de um intermediário, como o IIS. O modelo de programação especifica a sequência de atividades necessárias para atingir essa meta. O modelo de objeto especifica os objetos cujos métodos e propriedades afetam o modelo de programação.</span><span class="sxs-lookup"><span data-stu-id="876d7-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="876d7-107">O RDS permite executar a sequência de ações a seguir:</span><span class="sxs-lookup"><span data-stu-id="876d7-107">RDS provides the means to perform the following sequence of actions:</span></span>

- <span data-ttu-id="876d7-108">Especifique o programa a ser chamado no servidor e encontre uma maneira (proxy) de fazer referência a ele a partir do cliente ([RDS.DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="876d7-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

- <span data-ttu-id="876d7-p102">Chame o programa de servidor. Passe parâmetros para o programa de servidor que identifica a fonte de dados e o comando a ser emitido (proxy ou [RDS.DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="876d7-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

- <span data-ttu-id="876d7-p103">O programa de servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados, geralmente usando o ADO. Opcionalmente, o objeto **Recordset** será processado no servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="876d7-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

- <span data-ttu-id="876d7-113">O programa de servidor retorna o objeto **Recordset** final ao aplicativo cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="876d7-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

- <span data-ttu-id="876d7-114">No cliente, o objeto **Recordset** é colocado em um formato que pode ser facilmente usado por controles visuais (controle visual e **RDS.DataControl**).</span><span class="sxs-lookup"><span data-stu-id="876d7-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

- <span data-ttu-id="876d7-115">As alterações feitas no objeto **Recordset** são reenviadas ao servidor e usadas para atualizar a fonte de dados (**RDS.DataControl** ou **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="876d7-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

