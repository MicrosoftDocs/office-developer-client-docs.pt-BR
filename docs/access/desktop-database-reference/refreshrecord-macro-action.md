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
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721559"
---
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="03107-102">Ação da macro AtualizarRegistro</span><span class="sxs-lookup"><span data-stu-id="03107-102">RefreshRecord macro action</span></span>


<span data-ttu-id="03107-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="03107-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03107-104">Você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="03107-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="03107-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="03107-105">Remarks</span></span>

<span data-ttu-id="03107-p101">A ação **AtualizarRegistro** mostra somente as alterações feitas em registros no conjunto atual. Como a ação **AtualizarRegistro** não repete consultas ao banco de dados, o conjunto atual não incluirá registros que foram adicionados nem excluirá registros que foram excluídos após a última repetição de consulta ao banco de dados. Além disso, não excluirá os registros que não mais satisfaçam os critérios da consulta ou do filtro. Para repetir a consulta ao banco de dados, utilize o método **[Repetir consulta](requery-macro-action.md)**. Quando a fonte do registro de um formulário for consultada novamente, o conjunto atual de registros refletirá corretamente todos os dados da fonte do registro. .</span><span class="sxs-lookup"><span data-stu-id="03107-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="03107-110">O comportamento desta ação de macro depende do fato de estar sendo chamada em um banco de dados cliente ou em um banco de dados da Web.</span><span class="sxs-lookup"><span data-stu-id="03107-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="03107-111">Banco de dados cliente</span><span class="sxs-lookup"><span data-stu-id="03107-111">Client database</span></span>

<span data-ttu-id="03107-p102">Em um banco de dados cliente, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos dados no conjunto atual. É equivalente ao método **[Atualizar](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**.</span><span class="sxs-lookup"><span data-stu-id="03107-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="03107-115">A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados cliente:</span><span class="sxs-lookup"><span data-stu-id="03107-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="03107-p103">Atualiza a fonte do registro para o formulário ou para a folha de dados ativa para refletir as alterações feitas nas linhas do conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="03107-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="03107-118">Atualiza o conjunto atual para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="03107-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="03107-119">Se uma linha em uma fonte de registro tiver sido excluída, ele será alterado para mostrar \#Deleted.</span><span class="sxs-lookup"><span data-stu-id="03107-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="03107-120">Atualiza o ativo ou folha de dados para exibir quaisquer registros alterados e qualquer \#excluídos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="03107-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="03107-121">Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.</span><span class="sxs-lookup"><span data-stu-id="03107-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="03107-122">Banco de dados da Web</span><span class="sxs-lookup"><span data-stu-id="03107-122">Web database</span></span>

<span data-ttu-id="03107-p105">Em um banco de dados da Web, você pode usar a ação **AtualizarRegistro** para atualizar a fonte do registro subjacente do formulário ou da folha de dados ativa para refletir alterações feitas nos registros no conjunto atual. As alterações incluem aquelas feitas pelo usuário atual ou por outros usuários.</span><span class="sxs-lookup"><span data-stu-id="03107-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="03107-125">A ação de macro **AtualizarRegistro** executa as seguintes ações em um banco de dados da Web:</span><span class="sxs-lookup"><span data-stu-id="03107-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="03107-p106">Recupera alterações do servidor para quaisquer tabelas de base no conjunto atual. Para tabelas ODBC vinculadas, recuperada alterações nos registros no conjunto atual da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="03107-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="03107-128">Atualiza o conjunto atual para refletir as alterações.</span><span class="sxs-lookup"><span data-stu-id="03107-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="03107-129">Se uma linha no conjunto atual tiver sido excluída, ele será alterado para mostrar \#Deleted.</span><span class="sxs-lookup"><span data-stu-id="03107-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="03107-130">Atualiza a ativa formulário ou folha de dados para exibir quaisquer registros alterados e qualquer \#excluídos registros no conjunto atual.</span><span class="sxs-lookup"><span data-stu-id="03107-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="03107-131">Repete consultas em todos os subformulários e subrelatórios no formulário ou na folha de dados ativa.</span><span class="sxs-lookup"><span data-stu-id="03107-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

