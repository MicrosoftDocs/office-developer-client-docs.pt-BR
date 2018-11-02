---
title: Método TableDefs.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a632999f1b60b078e9365c9f99e52ddec284e9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927876"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="875c8-102">Método TableDefs.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="875c8-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="875c8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="875c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="875c8-104">Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="875c8-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="875c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="875c8-105">Syntax</span></span>

<span data-ttu-id="875c8-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="875c8-106">*expression* .Refresh</span></span>

<span data-ttu-id="875c8-107">*expressão* Uma variável que representa um objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="875c8-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="875c8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="875c8-108">Remarks</span></span>

<span data-ttu-id="875c8-p101">Para determinar a posição que o mecanismo de banco de dados do Microsoft Access usa para os objetos **Field** na coleção **Fields** de um objeto **QueryDef**, **Recordset** ou **TableDef**, utilize a propriedade **OrdinalPosition** de cada objeto **Field**. Alterar a propriedade **OrdinalPosition** de um objeto **Field** pode não alterar a ordem dos objetos **Field** na coleção até que você use o método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="875c8-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="875c8-p102">Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="875c8-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="875c8-p103">Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="875c8-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

