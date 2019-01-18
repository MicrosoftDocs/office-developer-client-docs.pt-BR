---
title: Método Documents.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 33405192-f23c-e2a2-feb6-9d641439cbc5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192321(v=office.15)
ms:contentKeyID: 48544100
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1e0ecf94a2442d742475bdf00311bbfa1e222f2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719180"
---
# <a name="documentsrefresh-method-dao"></a><span data-ttu-id="867cb-102">Método Documents.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="867cb-102">Documents.Refresh method (DAO)</span></span>


<span data-ttu-id="867cb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="867cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="867cb-104">Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="867cb-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="867cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="867cb-105">Syntax</span></span>

<span data-ttu-id="867cb-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="867cb-106">*expression* .Refresh</span></span>

<span data-ttu-id="867cb-107">*expressão* Uma variável que representa um objeto **Documents** .</span><span class="sxs-lookup"><span data-stu-id="867cb-107">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="867cb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="867cb-108">Remarks</span></span>

<span data-ttu-id="867cb-p101">Use o método **Refresh** em ambientes multiusuários nos quais outros usuários podem alterar o banco de dados. Talvez seja necessário usá-lo em coleções indiretamente afetadas por alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, talvez seja necessário atualizar uma coleção **Groups** antes de usar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="867cb-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="867cb-p102">Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="867cb-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

