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
ms.openlocfilehash: ee9afcd5367135da2d39fe889d17d089ae6f4c25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462300"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="4511f-102">Propriedade Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="4511f-102">Recordset2.Type Property (DAO)</span></span>


<span data-ttu-id="4511f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4511f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4511f-p101">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4511f-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4511f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4511f-106">Syntax</span></span>

<span data-ttu-id="4511f-107">*expressão* . Tipo</span><span class="sxs-lookup"><span data-stu-id="4511f-107">*expression* .Type</span></span>

<span data-ttu-id="4511f-108">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="4511f-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4511f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4511f-109">Remarks</span></span>

<span data-ttu-id="4511f-110">Para um objeto **Recordset**, as configurações e os valores de retorno possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="4511f-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4511f-111">Constante</span><span class="sxs-lookup"><span data-stu-id="4511f-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="4511f-112">Tipo de Recordset</span><span class="sxs-lookup"><span data-stu-id="4511f-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4511f-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="4511f-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="4511f-114">Tabela (somente em espaços de trabalho do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="4511f-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4511f-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="4511f-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="4511f-116">Dinâmico (somente em espaços de trabalho ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="4511f-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="4511f-p102">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4511f-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4511f-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="4511f-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="4511f-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="4511f-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4511f-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="4511f-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="4511f-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="4511f-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4511f-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="4511f-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="4511f-124">Somente de Encaminhamento</span><span class="sxs-lookup"><span data-stu-id="4511f-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

