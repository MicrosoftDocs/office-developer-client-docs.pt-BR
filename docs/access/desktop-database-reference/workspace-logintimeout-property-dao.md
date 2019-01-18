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
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="a90f5-102">Propriedade Workspace.LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="a90f5-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="a90f5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a90f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a90f5-104">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="a90f5-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a90f5-105">Syntax</span></span>

<span data-ttu-id="a90f5-106">*expressão* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="a90f5-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="a90f5-107">*expressão* Uma variável que representa um objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="a90f5-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a90f5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a90f5-108">Remarks</span></span>

<span data-ttu-id="a90f5-p101">A definição da propriedade **LoginTimeout** padrão é de 20 segundos. Quando a propriedade **LoginTimeout** estiver definida como 0, não haverá tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a90f5-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="a90f5-p102">Quando você estiver tentando fazer logon em um banco de dados ODBC, como o Microsoft SQL Server, a conexão poderá falhar como resultado de erros de rede ou porque o servidor não estava em execução. Em vez de aguardar os 20 segundos padrão para se conectar, especifique quanto tempo será necessário aguardar antes da ocorrência de um erro. O logon no servidor acontece de forma implícita como parte de diversos eventos diferentes, como a execução de uma consulta em um banco de dados de servidor externo.</span><span class="sxs-lookup"><span data-stu-id="a90f5-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

