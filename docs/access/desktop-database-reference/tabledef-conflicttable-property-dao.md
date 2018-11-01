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
ms.openlocfilehash: 81b7793291575ca86b5eec628ac9472a20d90ce4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870657"
---
# <a name="tabledefconflicttable-property-dao"></a>Propriedade TableDef.ConflictTable (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Retorna o nome de uma tabela em conflito que contém os registros do banco de dados que estavam em conflito durante a sincronização de duas réplicas (apenas espaços de trabalho do Microsoft Access). **String** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . ConflictTable

*expressão* Uma expressão que retorna um objeto **TableDef** .

## <a name="remarks"></a>Comentários

O valor de retorno será um tipo de dados **String**, que é uma sequência com comprimento zero (""), se não houver nenhuma tabela conflitante ou se o banco de dados não for uma réplica.

Se dois usuários em duas réplicas separadas fizerem uma alteração no mesmo registro no banco de dados, as alterações feitas por um usuário não serão aplicadas à outra réplica. Consequentemente, o usuário cuja alteração não foi aplicada deve resolver os conflitos.

Os conflitos ocorrem no nível do registro, não entre os campos. Por exemplo, se um usuário altera o campo Endereço e o campo Telefone no mesmo registro, uma das alterações é recusada. Como os conflitos ocorrem no nível do registro, a recusa ocorra mesmo que a alteração aceita e a alteração recusada não resultem em um conflito de informações verdadeiro.

O mecanismo de sincronização manipula os conflitos do registro criando tabelas de conflito, que contêm as informações que devem ser colocadas na tabela se as alterações forem bem-sucedidas. Você pode examinar essas tabelas de conflitos e trabalhar nelas linha por linha, corrigindo o que for apropriado.

Todas as tabelas de conflito são denominadas tabela\_conflito, onde a tabela é o nome original da tabela, truncado para o comprimento de nome de tabela máximo.

