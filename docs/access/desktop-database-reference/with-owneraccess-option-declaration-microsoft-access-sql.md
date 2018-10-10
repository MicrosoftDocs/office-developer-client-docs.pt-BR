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
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>Declaração WITH OWNERACCESS OPTION (Microsoft Access SQL)


**Aplica-se a**: Access 2013 | Office 2013

Em um ambiente de vários usuários com um grupo de trabalho seguro, use essa declaração com uma consulta para fornecer ao usuário que executa a consulta as mesmas permissões do proprietário da consulta.

## <a name="syntax"></a>Sintaxe

*SQLStatement* COM OWNERACCESS OPTION

## <a name="remarks"></a>Comentários

A declaração WITH OWNERACCESS OPTION é opcional.

O exemplo a seguir permite que o usuário exiba informações sobre salário (mesmo que o usuário não tenha permissão para exibir a tabela Folha de Pagamento), desde que o proprietário da consulta tenha essa permissão:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Se um usuário for impedido que criar uma tabela ou fazer acréscimos a ela, você poderá usar WITH OWNERACCESS OPTION para permitir que o usuário execute a criação de uma tabela ou a consulta acréscimo.

Se você quiser aplicar as configurações de segurança do grupo de trabalho e as permissões do usuário, não inclua a declaração WITH OWNERACCESS OPTION.

Essa opção exige que você tenha acesso ao arquivo System.mdw associado ao banco de dados. Ele é útil somente em implementações seguras em ambientes de vários usuários.

