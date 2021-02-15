---
title: Método Relations.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9da7cdcead4f5143674f4b46f4a57d5c32dc62fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306766"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="821af-102">Método Relations.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="821af-102">Relations.Refresh method (DAO)</span></span>


<span data-ttu-id="821af-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="821af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="821af-104">Atualiza os objetos na coleta especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="821af-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="821af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="821af-105">Syntax</span></span>

<span data-ttu-id="821af-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="821af-106">*expression* .Refresh</span></span>

<span data-ttu-id="821af-107">*expressão* Uma variável que representa um **objeto Relations** .</span><span class="sxs-lookup"><span data-stu-id="821af-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="821af-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="821af-108">Remarks</span></span>

<span data-ttu-id="821af-p101">Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="821af-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="821af-p102">Uma coleção é preenchida com objetos quando ela se refere, pela primeira vez, a e não reflete automaticamente as alterações subsequentes feitas por outros usuários. Se provavelmente outro usuário alterou uma coleção, use o método Refresh na coleção imediatamente antes de executar qualquer tarefa no aplicativo que considera a presença ou a ausência de um objeto particular na coleção. Isso garante que a coleção seja atualizada assim que possível. Por outro lado, utilizar Refresh pode desnecessariamente reduzir o desempenho.</span><span class="sxs-lookup"><span data-stu-id="821af-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

