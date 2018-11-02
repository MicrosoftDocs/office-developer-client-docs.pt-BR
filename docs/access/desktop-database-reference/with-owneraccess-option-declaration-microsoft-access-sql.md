---
title: COM a declaração OWNERACCESS OPTION (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
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
ms.openlocfilehash: 0eca4738d07c54b049073aaf5d4b802864761fa5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920596"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a><span data-ttu-id="be4dd-102">COM a declaração OWNERACCESS OPTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="be4dd-102">WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="be4dd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="be4dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be4dd-104">Em um ambiente de vários usuários com um grupo de trabalho seguro, use essa declaração com uma consulta para fornecer ao usuário que executa a consulta as mesmas permissões do proprietário da consulta.</span><span class="sxs-lookup"><span data-stu-id="be4dd-104">In a multiuser environment with a secure workgroup, use this declaration with a query to give the user who runs the query the same permissions as the query's owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be4dd-105">Syntax</span></span>

<span data-ttu-id="be4dd-106">*SQLStatement* COM OWNERACCESS OPTION</span><span class="sxs-lookup"><span data-stu-id="be4dd-106">*sqlstatement* WITH OWNERACCESS OPTION</span></span>

## <a name="remarks"></a><span data-ttu-id="be4dd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="be4dd-107">Remarks</span></span>

<span data-ttu-id="be4dd-108">A declaração WITH OWNERACCESS OPTION é opcional.</span><span class="sxs-lookup"><span data-stu-id="be4dd-108">The WITH OWNERACCESS OPTION declaration is optional.</span></span>

<span data-ttu-id="be4dd-109">O exemplo a seguir permite que o usuário exiba informações sobre salário (mesmo que o usuário não tenha permissão para exibir a tabela Folha de Pagamento), desde que o proprietário da consulta tenha essa permissão:</span><span class="sxs-lookup"><span data-stu-id="be4dd-109">The following example enables the user to view salary information (even if the user does not otherwise have permission to view the Payroll table), provided that the query's owner does have that permission:</span></span>

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

<span data-ttu-id="be4dd-110">Se um usuário for impedido que criar uma tabela ou fazer acréscimos a ela, você poderá usar WITH OWNERACCESS OPTION para permitir que o usuário execute a criação de uma tabela ou a consulta acréscimo.</span><span class="sxs-lookup"><span data-stu-id="be4dd-110">If a user is otherwise prevented from creating or adding to a table, you can use WITH OWNERACCESS OPTION to enable the user to run a make-table or append query.</span></span>

<span data-ttu-id="be4dd-111">Se você quiser aplicar as configurações de segurança do grupo de trabalho e as permissões do usuário, não inclua a declaração WITH OWNERACCESS OPTION.</span><span class="sxs-lookup"><span data-stu-id="be4dd-111">If you want to enforce workgroup security settings and users' permissions, do not include the WITH OWNERACCESS OPTION declaration.</span></span>

<span data-ttu-id="be4dd-p101">Essa opção exige que você tenha acesso ao arquivo System.mdw associado ao banco de dados. Ele é útil somente em implementações seguras em ambientes de vários usuários.</span><span class="sxs-lookup"><span data-stu-id="be4dd-p101">This option requires you to have access to the System.mdw file associated with the database. It is useful only in secured multiuser implementations.</span></span>

