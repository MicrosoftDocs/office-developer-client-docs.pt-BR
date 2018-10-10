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
ms.openlocfilehash: 53df33e3171cde0d861f738a852350ec20bf0dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463125"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="0711f-102">Propriedade LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="0711f-102">DBEngine.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="0711f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0711f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0711f-104">Define ou retorna o número de segundos antes de ocorrer um erro durante a tentativa de fazer logon em um banco de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="0711f-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0711f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0711f-105">Syntax</span></span>

<span data-ttu-id="0711f-106">*expressão* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="0711f-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="0711f-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0711f-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0711f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0711f-108">Remarks</span></span>

<span data-ttu-id="0711f-p101">A definição da propriedade **LoginTimeout** padrão é de 20 segundos. Quando a propriedade **LoginTimeout** estiver definida como 0, não haverá tempo limite.</span><span class="sxs-lookup"><span data-stu-id="0711f-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="0711f-p102">Quando você estiver tentando fazer logon em um banco de dados ODBC, como o Microsoft SQL Server, a conexão poderá falhar como resultado de erros de rede ou porque o servidor não estava em execução. Em vez de aguardar os 20 segundos padrão para se conectar, especifique quanto tempo será necessário aguardar antes da ocorrência de um erro. O logon no servidor acontece de forma implícita como parte de diversos eventos diferentes, como a execução de uma consulta em um banco de dados de servidor externo.</span><span class="sxs-lookup"><span data-stu-id="0711f-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

