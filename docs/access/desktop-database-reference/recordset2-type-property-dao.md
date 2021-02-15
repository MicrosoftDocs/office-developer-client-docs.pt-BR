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
localization_priority: Normal
ms.openlocfilehash: 6646658daf482373ef8b62f6d3420b1d11152cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307172"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="5dc8b-102">Propriedade Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="5dc8b-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="5dc8b-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dc8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dc8b-104">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="5dc8b-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="5dc8b-105">**Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5dc8b-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc8b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dc8b-106">Syntax</span></span>

<span data-ttu-id="5dc8b-107">*expressão* .Type</span><span class="sxs-lookup"><span data-stu-id="5dc8b-107">*expression* .Type</span></span>

<span data-ttu-id="5dc8b-108">*expressão* Uma variável que representa **um objeto Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="5dc8b-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc8b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dc8b-109">Remarks</span></span>

<span data-ttu-id="5dc8b-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="5dc8b-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dc8b-111">Constant</span><span class="sxs-lookup"><span data-stu-id="5dc8b-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="5dc8b-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="5dc8b-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc8b-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="5dc8b-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc8b-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="5dc8b-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc8b-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="5dc8b-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc8b-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="5dc8b-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="5dc8b-117"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="5dc8b-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="5dc8b-118">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5dc8b-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc8b-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="5dc8b-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc8b-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="5dc8b-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc8b-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="5dc8b-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc8b-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="5dc8b-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc8b-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="5dc8b-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc8b-124">Somente encaminhamento</span><span class="sxs-lookup"><span data-stu-id="5dc8b-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

