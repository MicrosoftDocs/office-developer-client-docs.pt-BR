---
title: Método TableDefs. Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306311"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="00d80-102">Método TableDefs. Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="00d80-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="00d80-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00d80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00d80-104">Atualiza os objetos na coleta especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="00d80-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d80-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00d80-105">Syntax</span></span>

<span data-ttu-id="00d80-106">*expressão* . Atualizado</span><span class="sxs-lookup"><span data-stu-id="00d80-106">*expression* .Refresh</span></span>

<span data-ttu-id="00d80-107">*expressão* Uma variável que representa um \*\*\*\* objeto TableDefs.</span><span class="sxs-lookup"><span data-stu-id="00d80-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d80-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="00d80-108">Remarks</span></span>

<span data-ttu-id="00d80-p101">Para determinar a posição que o mecanismo de banco de dados do Microsoft Access usa para os objetos **Field** na coleção **Fields** de um objeto **QueryDef**, **Recordset** ou **TableDef**, utilize a propriedade **OrdinalPosition** de cada objeto **Field**. Alterar a propriedade **OrdinalPosition** de um objeto **Field** pode não alterar a ordem dos objetos **Field** na coleção até que você use o método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="00d80-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="00d80-p102">Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="00d80-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="00d80-p103">Uma coleção é preenchida com objetos quando ela se refere, pela primeira vez, a e não reflete automaticamente as alterações subsequentes feitas por outros usuários. Se provavelmente outro usuário alterou uma coleção, use o método Refresh na coleção imediatamente antes de executar qualquer tarefa no aplicativo que considera a presença ou a ausência de um objeto particular na coleção. Isso garante que a coleção seja atualizada assim que possível. Por outro lado, utilizar Refresh pode desnecessariamente reduzir o desempenho.</span><span class="sxs-lookup"><span data-stu-id="00d80-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

