---
title: Propriedade Connection.QueryTimeout (DAO)
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
ms.openlocfilehash: 8f5ce9faa1ebd56bdc8e4de5aeea417835c950b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878805"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="536eb-102">Propriedade Connection.QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="536eb-102">Connection.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="536eb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="536eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="536eb-104">Define ou retorna um valor que especifica o número de segundos a serem aguardados antes de ocorrer um erro de tempo limite quando uma consulta é executada em uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="536eb-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="536eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="536eb-105">Syntax</span></span>

<span data-ttu-id="536eb-106">*expressão* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="536eb-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="536eb-107">*expressão* Uma variável que representa um objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="536eb-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="536eb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="536eb-108">Remarks</span></span>

<span data-ttu-id="536eb-109">O valor padrão é 60.</span><span class="sxs-lookup"><span data-stu-id="536eb-109">The default value is 60.</span></span>

<span data-ttu-id="536eb-p101">Quando você está utilizando um banco de dados ODBC, como o Microsoft SQL Server, pode haver atrasos devido ao tráfego da rede ou ao uso pesado do servidor ODBC. Em vez aguardar por um tempo indefinido, você poderá especificar o tempo de espera.</span><span class="sxs-lookup"><span data-stu-id="536eb-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="536eb-p102">Quando você usar **QueryTimeout** com um objeto **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, essa propriedade especificará um valor global para todas as consultas associadas ao banco de dados. É possível substituir esse valor para uma consulta específica pela definição da propriedade **ODBCTimeout** de um objeto **[QueryDef](querydef-object-dao.md)** específico.</span><span class="sxs-lookup"><span data-stu-id="536eb-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

