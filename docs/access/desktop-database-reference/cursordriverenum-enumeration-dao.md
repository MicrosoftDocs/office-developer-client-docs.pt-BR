---
title: Enumeração CursorDriverEnum (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d264c1e91982231e025f17c00db79e47a1d5c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880737"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="8d314-102">Enumeração CursorDriverEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d314-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="8d314-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d314-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d314-104">Especifica o tipo de driver de cursor.</span><span class="sxs-lookup"><span data-stu-id="8d314-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d314-105">Nome</span><span class="sxs-lookup"><span data-stu-id="8d314-105">Name</span></span></p></th>
<th><p><span data-ttu-id="8d314-106">Valor</span><span class="sxs-lookup"><span data-stu-id="8d314-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8d314-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d314-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d314-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="8d314-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="8d314-109">3</span><span class="sxs-lookup"><span data-stu-id="8d314-109">3</span></span></p></td>
<td><p><span data-ttu-id="8d314-p101">Sempre utiliza a Biblioteca de Cursores do FoxPro. Esta opção é necessária para executar atualizações em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d314-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d314-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="8d314-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="8d314-113">-1</span><span class="sxs-lookup"><span data-stu-id="8d314-113">-1</span></span></p></td>
<td><p><span data-ttu-id="8d314-114">(Padrão) Utiliza cursores do servidor se este oferecer suporte; caso contrário, usa a Biblioteca de Cursores ODBC.</span><span class="sxs-lookup"><span data-stu-id="8d314-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d314-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="8d314-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="8d314-116">4</span><span class="sxs-lookup"><span data-stu-id="8d314-116">4</span></span></p></td>
<td><p><span data-ttu-id="8d314-117">Abre todos os cursores (ou seja, objetos <strong>Recordset</strong> ) como tipo somente de encaminhamento, como somente leitura, com um tamanho de conjunto de linhas de 1.</span><span class="sxs-lookup"><span data-stu-id="8d314-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="8d314-118">Também conhecido como &quot;consultas sem cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="8d314-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d314-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="8d314-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="8d314-120">1</span><span class="sxs-lookup"><span data-stu-id="8d314-120">1</span></span></p></td>
<td><p><span data-ttu-id="8d314-p103">Sempre utiliza a Biblioteca de Cursores ODBC. Esta opção fornece melhor desempenho para pequenos conjuntos de resultados, mas se degrada rapidamente em conjuntos de resultados maiores.</span><span class="sxs-lookup"><span data-stu-id="8d314-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d314-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="8d314-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="8d314-124">2</span><span class="sxs-lookup"><span data-stu-id="8d314-124">2</span></span></p></td>
<td><p><span data-ttu-id="8d314-p104">Sempre utiliza cursores do servidor. Para a maioria das grandes operações esta opção oferece melhor desempenho, mas pode gerar mais tráfego na rede.</span><span class="sxs-lookup"><span data-stu-id="8d314-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

