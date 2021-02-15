---
title: Método Query (RDS - referência do banco de dados da área de trabalho do Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301110"
---
# <a name="query-method-rds"></a><span data-ttu-id="51ba6-102">Método Query (RDS)</span><span class="sxs-lookup"><span data-stu-id="51ba6-102">Query method (RDS)</span></span>

<span data-ttu-id="51ba6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51ba6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51ba6-104">Utiliza uma sequência de consulta SQL válida para retornar um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="51ba6-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="51ba6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51ba6-105">Syntax</span></span>

<span data-ttu-id="51ba6-106">Definir *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)</span><span class="sxs-lookup"><span data-stu-id="51ba6-106">Set *Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="51ba6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51ba6-107">Parameters</span></span>

|<span data-ttu-id="51ba6-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="51ba6-108">Parameter</span></span>|<span data-ttu-id="51ba6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="51ba6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="51ba6-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="51ba6-110">*Recordset*</span></span> |<span data-ttu-id="51ba6-111">Uma variável de objeto que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="51ba6-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="51ba6-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="51ba6-112">*DataFactory*</span></span> |<span data-ttu-id="51ba6-113">Uma variável de objeto que representa um objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="51ba6-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="51ba6-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="51ba6-114">*Connection*</span></span> |<span data-ttu-id="51ba6-p101">Um valor **String** que contém as informações de conexão do servidor. Isso é semelhante à propriedade [Connect](connect-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="51ba6-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="51ba6-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="51ba6-117">*Query*</span></span> |<span data-ttu-id="51ba6-118">Uma **String** que contém a consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="51ba6-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="51ba6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ba6-119">Remarks</span></span>

<span data-ttu-id="51ba6-p102">A consulta deve utilizar o dialeto SQL do servidor de banco de dados. Um status de resultado será retornado se houver um erro com a consulta que foi executada. O método **Query** não desempenha nenhuma verificação de sintaxe na sequência **Query**.</span><span class="sxs-lookup"><span data-stu-id="51ba6-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

