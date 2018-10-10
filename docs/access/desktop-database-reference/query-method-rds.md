---
title: Método Query (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a9ecb2d7ebfdd8f6738b8d7b9b8738ce981ec16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462432"
---
# <a name="query-method-rds"></a><span data-ttu-id="6fb5d-102">Método Query (RDS)</span><span class="sxs-lookup"><span data-stu-id="6fb5d-102">Query Method (RDS)</span></span>


<span data-ttu-id="6fb5d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fb5d-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6fb5d-104">Utiliza uma sequência de consulta SQL válida para retornar um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6fb5d-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fb5d-105">Syntax</span></span>

<span data-ttu-id="6fb5d-106">Definir o*Recordset* = *DataFactory*. Consulta (*Conexão*, *consulta*)</span><span class="sxs-lookup"><span data-stu-id="6fb5d-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6fb5d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fb5d-107">Parameters</span></span>

  - <span data-ttu-id="6fb5d-108">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="6fb5d-108">*Recordset*</span></span>

  - <span data-ttu-id="6fb5d-109">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6fb5d-109">An object variable that represents a **Recordset** object.</span></span>

  - <span data-ttu-id="6fb5d-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="6fb5d-110">*DataFactory*</span></span>

  - <span data-ttu-id="6fb5d-111">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="6fb5d-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="6fb5d-112">*Connection*</span><span class="sxs-lookup"><span data-stu-id="6fb5d-112">*Connection*</span></span>

  - <span data-ttu-id="6fb5d-p101">Um valor **String** que contém as informações de conexão do servidor. Isso é semelhante à propriedade [Connect](connect-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="6fb5d-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>

  - <span data-ttu-id="6fb5d-115">*Query*</span><span class="sxs-lookup"><span data-stu-id="6fb5d-115">*Query*</span></span>

  - <span data-ttu-id="6fb5d-116">Uma **String** que contém a consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="6fb5d-116">A **String** that contains the SQL query.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb5d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fb5d-117">Remarks</span></span>

<span data-ttu-id="6fb5d-p102">A consulta deve utilizar o dialeto SQL do servidor de banco de dados. Um status de resultado será retornado se houver um erro com a consulta que foi executada. O método **Query** não desempenha nenhuma verificação de sintaxe na sequência **Query**.</span><span class="sxs-lookup"><span data-stu-id="6fb5d-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

