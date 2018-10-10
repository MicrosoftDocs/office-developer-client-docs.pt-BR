---
title: Declaração WITH OWNERACCESS OPTION (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b47b9fcc5b3c4422ec60bbdaf06193533c20b6e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464839"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="57473-102">Declaração WITH OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="57473-102">WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="57473-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="57473-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57473-104">Em um ambiente de vários usuários com um grupo de trabalho seguro, use essa declaração com uma consulta para fornecer ao usuário que executa a consulta as mesmas permissões do proprietário da consulta.</span><span class="sxs-lookup"><span data-stu-id="57473-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="57473-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57473-105">Syntax</span></span>

<span data-ttu-id="57473-106">*SQLStatement* COM OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="57473-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="57473-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="57473-107">Remarks</span></span>

<span data-ttu-id="57473-108">A declaração WITH OWNERACCESS OPTION é opcional.</span><span class="sxs-lookup"><span data-stu-id="57473-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="57473-109">O exemplo a seguir permite que o usuário exiba informações sobre salário (mesmo que o usuário não tenha permissão para exibir a tabela Folha de Pagamento), desde que o proprietário da consulta tenha essa permissão:</span><span class="sxs-lookup"><span data-stu-id="57473-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="57473-110">Se um usuário for impedido que criar uma tabela ou fazer acréscimos a ela, você poderá usar WITH OWNERACCESS OPTION para permitir que o usuário execute a criação de uma tabela ou a consulta acréscimo.</span><span class="sxs-lookup"><span data-stu-id="57473-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="57473-111">Se você quiser aplicar as configurações de segurança do grupo de trabalho e as permissões do usuário, não inclua a declaração WITH OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="57473-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="57473-p101">Essa opção exige que você tenha acesso ao arquivo System.mdw associado ao banco de dados. Ele é útil somente em implementações seguras em ambientes de vários usuários.</span><span class="sxs-lookup"><span data-stu-id="57473-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

