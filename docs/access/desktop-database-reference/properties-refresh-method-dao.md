---
title: Método Properties.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4df20311746b562d319e371da3cf75b452c064e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462834"
---
# <a name="propertiesrefresh-method-dao"></a><span data-ttu-id="0a788-102">Método Properties.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a788-102">Properties.Refresh Method (DAO)</span></span>


<span data-ttu-id="0a788-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a788-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a788-104">Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0a788-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a788-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a788-105">Syntax</span></span>

<span data-ttu-id="0a788-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="0a788-106">*expression* .Refresh</span></span>

<span data-ttu-id="0a788-107">*expressão* Uma variável que representa um objeto **Properties** .</span><span class="sxs-lookup"><span data-stu-id="0a788-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a788-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a788-108">Remarks</span></span>

<span data-ttu-id="0a788-p101">Use o método **Refresh** em ambientes multiusuários nos quais outros usuários podem alterar o banco de dados. Talvez seja necessário usá-lo em coleções indiretamente afetadas por alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, talvez seja necessário atualizar uma coleção **Groups** antes de usar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="0a788-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="0a788-p102">Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="0a788-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

