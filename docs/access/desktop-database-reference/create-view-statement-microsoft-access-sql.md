---
title: Instrução CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5a25327aa81979a81f3410a383c06a0eda9d3113
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873737"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="9b4c3-102">Instrução CREATE VIEW (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9b4c3-102">CREATE VIEW statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="9b4c3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b4c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b4c3-104">Cria uma nova exibição.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="9b4c3-105">[!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE VIEW nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4c3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b4c3-106">Syntax</span></span>

<span data-ttu-id="9b4c3-107">*Modo de exibição* de CREATE VIEW \[(*field1*\[, *field2*\[,... \] \])\] Como *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="9b4c3-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="9b4c3-108">A instrução CREATE VIEW contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="9b4c3-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b4c3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9b4c3-109">Part</span></span></p></th>
<th><p><span data-ttu-id="9b4c3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b4c3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b4c3-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="9b4c3-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="9b4c3-112">O nome da exibição a ser criada.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b4c3-113"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="9b4c3-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="9b4c3-114">O nome do(s) campo(s) para a correspondência de campos especificada em <em>selectstatement</em>.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9b4c3-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="9b4c3-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="9b4c3-116">Uma instrução SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-116">A SQL SELECT statement.</span></span> <span data-ttu-id="9b4c3-117">Para obter mais informações, consulte a <a href="select-statement-microsoft-access-sql.md">instrução SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9b4c3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b4c3-118">Remarks</span></span>

<span data-ttu-id="9b4c3-119">A instrução SELECT que define a exibição não pode ser uma instrução [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="9b4c3-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="9b4c3-120">A instrução SELECT que define a exibição não pode conter nenhum parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="9b4c3-121">O nome do modo de exibição não pode ser igual ao nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="9b4c3-122">Se a consulta definida pela instrução SELECT for atualizável, a exibição também é atualizável.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="9b4c3-123">Caso contrário, a exibição será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="9b4c3-124">Se dois campos na consulta definida pela instrução SELECT tiverem o mesmo nome, a definição de exibição deverá incluir uma lista de campos que especifique nomes exclusivos para cada um dos campos na consulta.</span><span class="sxs-lookup"><span data-stu-id="9b4c3-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

