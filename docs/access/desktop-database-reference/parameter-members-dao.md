---
title: Membros do parâmetro (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707903"
---
# <a name="parameter-members-dao"></a><span data-ttu-id="7c121-102">Membros do parâmetro (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c121-102">Parameter members (DAO)</span></span>

<span data-ttu-id="7c121-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c121-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c121-p101">Um objeto Parameter representa um valor fornecido para uma consulta. O parâmetro está associado ao objeto QueryDef criado a partir de uma consulta parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7c121-p101">A Parameter object represents a value supplied to a query. The parameter is associated with a QueryDef object created from a parameter query.</span></span>

## <a name="properties"></a><span data-ttu-id="7c121-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7c121-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c121-107">Nome</span><span class="sxs-lookup"><span data-stu-id="7c121-107">Name</span></span></p></th>
<th><p><span data-ttu-id="7c121-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c121-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c121-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span><span class="sxs-lookup"><span data-stu-id="7c121-109"><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7c121-110"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="7c121-110"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="7c121-111">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7c121-111">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="7c121-112">Define ou retorna um valor que indica se um objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa um parâmetro de entrada, um parâmetro de saída, ambos ou o valor de retorno do procedimento (apenas espaços de trabalho do ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="7c121-112">Sets or returns a value that indicates whether a <strong><a href="parameter-object-dao.md">Parameter</a></strong> object represents an input parameter, an output parameter, both, or the return value from the procedure (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c121-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="7c121-113"><strong><a href="parameter-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7c121-p103">Retorna o nome do objeto especificado. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7c121-p103">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c121-116"><strong><a href="parameter-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="7c121-116"><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7c121-p104">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7c121-p104">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c121-119"><strong><a href="parameter-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="7c121-119"><strong><a href="parameter-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7c121-p105">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7c121-p105">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c121-122"><strong><a href="parameter-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="7c121-122"><strong><a href="parameter-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7c121-p106">Define ou retorna o valor de um objeto. <strong>Variant</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7c121-p106">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

