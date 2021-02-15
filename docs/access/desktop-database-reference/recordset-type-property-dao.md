---
title: Propriedade Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307550"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="8433d-102">Propriedade Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="8433d-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="8433d-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8433d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8433d-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8433d-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="8433d-105">**Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8433d-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8433d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8433d-106">Syntax</span></span>

<span data-ttu-id="8433d-107">*expressão* .Type</span><span class="sxs-lookup"><span data-stu-id="8433d-107">*expression* .Type</span></span>

<span data-ttu-id="8433d-108">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8433d-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8433d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8433d-109">Remarks</span></span>

<span data-ttu-id="8433d-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8433d-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8433d-111">Constant</span><span class="sxs-lookup"><span data-stu-id="8433d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="8433d-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="8433d-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8433d-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="8433d-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="8433d-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="8433d-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8433d-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="8433d-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="8433d-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="8433d-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="8433d-117"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8433d-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8433d-118">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8433d-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8433d-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="8433d-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="8433d-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="8433d-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8433d-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="8433d-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="8433d-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="8433d-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8433d-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8433d-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="8433d-124">Somente encaminhamento</span><span class="sxs-lookup"><span data-stu-id="8433d-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

