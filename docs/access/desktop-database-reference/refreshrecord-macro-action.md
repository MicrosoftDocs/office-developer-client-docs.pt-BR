---
title: Ação da macro AtualizarRegistro
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4b7ec534579b070d342fe2efd80af44e2ea921ef
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927267"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="40db1-102">Ação da macro AtualizarRegistro</span><span class="sxs-lookup"><span data-stu-id="40db1-102">RefreshRecord macro action</span></span>


<span data-ttu-id="40db1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="40db1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40db1-104">Você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="40db1-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="40db1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="40db1-105">Remarks</span></span>

<span data-ttu-id="40db1-p101">A ação **AtualizarRegistro** mostra somente as alterações feitas em registros no conjunto atual. Como a ação **AtualizarRegistro** não repete consultas ao banco de dados, o conjunto atual não incluirá registros que foram adicionados nem excluirá registros que foram excluídos após a última repetição de consulta ao banco de dados. Além disso, não excluirá os registros que não mais satisfaçam os critérios da consulta ou do filtro. Para repetir a consulta ao banco de dados, utilize o método **[Repetir consulta](requery-macro-action.md)**. Quando a fonte do registro de um formulário for consultada novamente, o conjunto atual de registros refletirá corretamente todos os dados da fonte do registro. .</span><span class="sxs-lookup"><span data-stu-id="40db1-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="40db1-110">O comportamento desta ação de macro depende do fato de estar sendo chamada em um banco de dados cliente ou em um banco de dados da Web.</span><span class="sxs-lookup"><span data-stu-id="40db1-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="40db1-111">Banco de dados cliente</span><span class="sxs-lookup"><span data-stu-id="40db1-111">Client database</span></span>

<span data-ttu-id="40db1-p102">Em um banco de dados cliente, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos dados no conjunto atual. É equivalente ao método **[Atualizar](https://msdn.microsoft.com/library/ff836021\(v=office.15\))**.</span><span class="sxs-lookup"><span data-stu-id="40db1-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://msdn.microsoft.com/library/ff836021\(v=office.15\))** method.</span></span>

<span data-ttu-id="40db1-115">A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados cliente:</span><span class="sxs-lookup"><span data-stu-id="40db1-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="40db1-p103">Atualiza a fonte do registro para o formulário ou para a folha de dados ativa para refletir as alterações feitas nas linhas do conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="40db1-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="40db1-118">Atualiza o conjunto atual para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="40db1-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="40db1-119">Se uma linha em uma fonte de registro tiver sido excluída, ele será alterado para mostrar \#Deleted.</span><span class="sxs-lookup"><span data-stu-id="40db1-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="40db1-120">Atualiza o ativo ou folha de dados para exibir quaisquer registros alterados e qualquer \#excluídos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="40db1-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="40db1-121">Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.</span><span class="sxs-lookup"><span data-stu-id="40db1-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="40db1-122">Banco de dados da Web</span><span class="sxs-lookup"><span data-stu-id="40db1-122">Web database</span></span>

<span data-ttu-id="40db1-p105">Em um banco de dados da Web, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual. As alterações incluem aquelas feitas pelo usuário atual ou por outros usuários.</span><span class="sxs-lookup"><span data-stu-id="40db1-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="40db1-125">A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados da Web:</span><span class="sxs-lookup"><span data-stu-id="40db1-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="40db1-p106">Recupera alterações do servidor para quaisquer tabelas de base no conjunto atual. Para tabelas ODBC vinculadas, recuperada alterações nos registros no conjunto atual da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="40db1-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="40db1-128">Atualiza o conjunto atual para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="40db1-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="40db1-129">Se uma linha no conjunto atual tiver sido excluída, ele será alterado para mostrar \#Deleted.</span><span class="sxs-lookup"><span data-stu-id="40db1-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="40db1-130">Atualiza a ativa formulário ou folha de dados para exibir quaisquer registros alterados e qualquer \#excluídos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="40db1-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="40db1-131">Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.</span><span class="sxs-lookup"><span data-stu-id="40db1-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

