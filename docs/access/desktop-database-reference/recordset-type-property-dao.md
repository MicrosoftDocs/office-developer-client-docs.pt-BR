---
title: Propriedade Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3eedbab083807f91ffef78aab25d110db779188
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026082"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="c0d2b-102">Propriedade Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0d2b-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="c0d2b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0d2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0d2b-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d2b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0d2b-106">Syntax</span></span>

<span data-ttu-id="c0d2b-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="c0d2b-107">*expression* .Type</span></span>

<span data-ttu-id="c0d2b-108">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c0d2b-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0d2b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0d2b-109">Remarks</span></span>

<span data-ttu-id="c0d2b-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c0d2b-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0d2b-111">Constante</span><span class="sxs-lookup"><span data-stu-id="c0d2b-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="c0d2b-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="c0d2b-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0d2b-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="c0d2b-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="c0d2b-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="c0d2b-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0d2b-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="c0d2b-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="c0d2b-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="c0d2b-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="c0d2b-117"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c0d2b-118">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c0d2b-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0d2b-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="c0d2b-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="c0d2b-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="c0d2b-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0d2b-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="c0d2b-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="c0d2b-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="c0d2b-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0d2b-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="c0d2b-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="c0d2b-124">Somente de Encaminhamento</span><span class="sxs-lookup"><span data-stu-id="c0d2b-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

