---
title: Propriedade Recordset2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ca75e1b21e017dfbbbc5028d06a4799a9afd50f3
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936592"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="426fe-102">Propriedade Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="426fe-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="426fe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="426fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="426fe-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="426fe-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="426fe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="426fe-106">Syntax</span></span>

<span data-ttu-id="426fe-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="426fe-107">*expression* .Type</span></span>

<span data-ttu-id="426fe-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="426fe-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="426fe-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="426fe-109">Remarks</span></span>

<span data-ttu-id="426fe-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="426fe-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="426fe-111">Constante</span><span class="sxs-lookup"><span data-stu-id="426fe-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="426fe-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="426fe-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="426fe-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="426fe-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="426fe-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="426fe-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="426fe-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="426fe-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="426fe-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="426fe-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="426fe-117"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="426fe-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="426fe-118">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="426fe-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="426fe-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="426fe-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="426fe-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="426fe-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="426fe-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="426fe-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="426fe-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="426fe-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="426fe-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="426fe-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="426fe-124">Somente de Encaminhamento</span><span class="sxs-lookup"><span data-stu-id="426fe-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

