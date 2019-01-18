---
title: Método Indexes.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: ffe1bc79-5a56-2a70-c5ac-2f80b683adbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837325(v=office.15)
ms:contentKeyID: 48548973
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7e1b2a017342532f3eba1e14ce6097fea8ebffa8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709366"
---
# <a name="indexesrefresh-method-dao"></a><span data-ttu-id="dce7d-102">Método Indexes.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="dce7d-102">Indexes.Refresh method (DAO)</span></span>


<span data-ttu-id="dce7d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dce7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dce7d-104">Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dce7d-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dce7d-105">Syntax</span></span>

<span data-ttu-id="dce7d-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="dce7d-106">*expression* .Refresh</span></span>

<span data-ttu-id="dce7d-107">*expressão* Uma variável que representa um objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="dce7d-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce7d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dce7d-108">Remarks</span></span>

<span data-ttu-id="dce7d-p101">Use o método **Refresh** em ambientes multiusuários nos quais outros usuários podem alterar o banco de dados. Talvez seja necessário usá-lo em coleções indiretamente afetadas por alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, talvez seja necessário atualizar uma coleção **Groups** antes de usar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="dce7d-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="dce7d-p102">Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="dce7d-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

