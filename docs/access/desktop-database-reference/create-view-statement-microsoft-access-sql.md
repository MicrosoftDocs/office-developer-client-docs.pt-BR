---
title: Instrução CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295363"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="a726c-102">Instrução CREATE VIEW (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a726c-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a726c-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a726c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a726c-104">Cria uma nova exibição.</span><span class="sxs-lookup"><span data-stu-id="a726c-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="a726c-105">O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de CREATE VIEW ou de qualquer uma das instruções DDL com bancos de dados de mecanismos de banco de dados que não são do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a726c-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="a726c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a726c-106">Syntax</span></span>

<span data-ttu-id="a726c-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="a726c-107">CREATE VIEW *view [(field1* \[[, *field2*[, …]])] AS *selectstatement*</span></span>

<span data-ttu-id="a726c-108">A instrução CREATE VIEW tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="a726c-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a726c-109">Sair</span><span class="sxs-lookup"><span data-stu-id="a726c-109">Part</span></span></p></th>
<th><p><span data-ttu-id="a726c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a726c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a726c-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="a726c-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="a726c-112">O nome do modo de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a726c-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a726c-113"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="a726c-113"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="a726c-114">O nome do campo ou campos para os campos correspondentes especificados no <em>selectstatement</em>.</span><span class="sxs-lookup"><span data-stu-id="a726c-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a726c-115"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="a726c-115">AS <em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="a726c-116">Uma instrução SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="a726c-116">A SQL SELECT statement.</span></span> <span data-ttu-id="a726c-117">Para obter mais informações, confira <a href="select-statement-microsoft-access-sql.md">Instrução SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="a726c-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a726c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a726c-118">Remarks</span></span>

<span data-ttu-id="a726c-119">A instrução SELECT que define a exibição não pode ser uma instrução [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a726c-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="a726c-120">A declaração SELECT que define o modo de exibição não pode conter parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a726c-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="a726c-121">O nome da exibição não pode ser igual ao nome de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="a726c-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="a726c-122">Se a consulta definida pela instrução SELECT for atualizável, a exibição também será atualizável.</span><span class="sxs-lookup"><span data-stu-id="a726c-122">If the query defined by the SELECT statement is updatable, then the view is also updatable.</span></span> <span data-ttu-id="a726c-123">Caso contrário, o modo de exibição será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a726c-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="a726c-124">Se os dois campos na consulta definidos pela instrução SELECT tiverem o mesmo nome, a definição do modo de exibição deverá incluir uma lista de campos especificando nomes exclusivos para cada um dos campos na consulta.</span><span class="sxs-lookup"><span data-stu-id="a726c-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

