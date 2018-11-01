---
title: Propriedade LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8c6b7798419dc72dc28822741e2d038203ae257e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880716"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="b133c-102">Propriedade LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="b133c-102">DBEngine.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="b133c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b133c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b133c-104">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="b133c-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b133c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b133c-105">Syntax</span></span>

<span data-ttu-id="b133c-106">*expressão* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="b133c-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="b133c-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b133c-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b133c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b133c-108">Remarks</span></span>

<span data-ttu-id="b133c-p101">A definição da propriedade **LoginTimeout** padrão é de 20 segundos. Quando a propriedade **LoginTimeout** estiver definida como 0, não haverá tempo limite.</span><span class="sxs-lookup"><span data-stu-id="b133c-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="b133c-p102">Quando você estiver tentando fazer logon em um banco de dados ODBC, como o Microsoft SQL Server, a conexão poderá falhar como resultado de erros de rede ou porque o servidor não estava em execução. Em vez de aguardar os 20 segundos padrão para se conectar, especifique quanto tempo será necessário aguardar antes da ocorrência de um erro. O logon no servidor acontece de forma implícita como parte de diversos eventos diferentes, como a execução de uma consulta em um banco de dados de servidor externo.</span><span class="sxs-lookup"><span data-stu-id="b133c-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

