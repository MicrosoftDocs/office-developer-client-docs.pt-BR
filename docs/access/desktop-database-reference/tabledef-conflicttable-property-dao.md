---
title: Propriedade TableDef.ConflictTable (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718914"
---
# <a name="tabledefconflicttable-property-dao"></a><span data-ttu-id="875b4-102">Propriedade TableDef.ConflictTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="875b4-102">TableDef.ConflictTable property (DAO)</span></span>


<span data-ttu-id="875b4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="875b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="875b4-p101">Retorna o nome de uma tabela em conflito que contém os registros do banco de dados que estavam em conflito durante a sincronização de duas réplicas (apenas espaços de trabalho do Microsoft Access). **String** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="875b4-p101">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only). Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="875b4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="875b4-106">Syntax</span></span>

<span data-ttu-id="875b4-107">*expressão* . ConflictTable</span><span class="sxs-lookup"><span data-stu-id="875b4-107">*expression* .ConflictTable</span></span>

<span data-ttu-id="875b4-108">*expressão* Uma expressão que retorna um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="875b4-108">*expression* An expression that returns a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="875b4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="875b4-109">Remarks</span></span>

<span data-ttu-id="875b4-110">O valor de retorno será um tipo de dados **String**, que é uma sequência com comprimento zero (""), se não houver nenhuma tabela conflitante ou se o banco de dados não for uma réplica.</span><span class="sxs-lookup"><span data-stu-id="875b4-110">The return value is a **String** data type that is a zero-length string ("") if there is no conflict table or the database isn't a replica.</span></span>

<span data-ttu-id="875b4-p102">Se dois usuários em duas réplicas separadas fizerem uma alteração no mesmo registro no banco de dados, as alterações feitas por um usuário não serão aplicadas à outra réplica. Consequentemente, o usuário cuja alteração não foi aplicada deve resolver os conflitos.</span><span class="sxs-lookup"><span data-stu-id="875b4-p102">If two users at two separate replicas each make a change to the same record in the database, the changes made by one user will fail to be applied to the other replica. Consequently, the user with the failed change must resolve the conflicts.</span></span>

<span data-ttu-id="875b4-p103">Os conflitos ocorrem no nível do registro, não entre os campos. Por exemplo, se um usuário altera o campo Endereço e o campo Telefone no mesmo registro, uma das alterações é recusada. Como os conflitos ocorrem no nível do registro, a recusa ocorra mesmo que a alteração aceita e a alteração recusada não resultem em um conflito de informações verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="875b4-p103">Conflicts occur at the record level, not between fields. For example, if one user changes the Address field and another updates the Phone field in the same record, then one change is rejected. Because conflicts occur at the record level, the rejection occurs even though the successful change and the rejected change are unlikely to result in a true conflict of information.</span></span>

<span data-ttu-id="875b4-p104">O mecanismo de sincronização manipula os conflitos do registro criando tabelas de conflito, que contêm as informações que devem ser colocadas na tabela se as alterações forem bem-sucedidas. Você pode examinar essas tabelas de conflitos e trabalhar nelas linha por linha, corrigindo o que for apropriado.</span><span class="sxs-lookup"><span data-stu-id="875b4-p104">The synchronization mechanism handles the record conflicts by creating conflict tables, which contain the information that would have been placed in the table, if the change had been successful. You can examine these conflict tables and work through them row by row, fixing whatever is appropriate.</span></span>

<span data-ttu-id="875b4-118">Todas as tabelas de conflito são denominadas tabela\_conflito, onde a tabela é o nome original da tabela, truncado para o comprimento de nome de tabela máximo.</span><span class="sxs-lookup"><span data-stu-id="875b4-118">All conflict tables are named table\_conflict, where table is the original name of the table, truncated to the maximum table name length.</span></span>

