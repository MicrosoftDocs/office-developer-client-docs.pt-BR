---
title: Propriedade TableDef. ConflictTable (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308425"
---
# <a name="tabledefconflicttable-property-dao"></a>Propriedade TableDef. ConflictTable (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Retorna o nome de uma tabela em conflito que contém os registros do banco de dados que estavam em conflito durante a sincronização de duas réplicas (apenas espaços de trabalho do Microsoft Access). **String** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . ConflictTable

*expressão* Uma expressão que retorna um objeto **TableDef** .

## <a name="remarks"></a>Comentários

O valor de retorno será um tipo de dados **String**, que é uma sequência com comprimento zero (""), se não houver nenhuma tabela conflitante ou se o banco de dados não for uma réplica.

Se dois usuários em duas réplicas separadas fizerem uma alteração no mesmo registro no banco de dados, as alterações feitas por um usuário não serão aplicadas à outra réplica. Consequentemente, o usuário cuja alteração não foi aplicada deve resolver os conflitos.

Os conflitos ocorrem no nível do registro, não entre os campos. Por exemplo, se um usuário altera o campo Endereço e o campo Telefone no mesmo registro, uma das alterações é recusada. Como os conflitos ocorrem no nível do registro, a recusa ocorra mesmo que a alteração aceita e a alteração recusada não resultem em um conflito de informações verdadeiro.

O mecanismo de sincronização manipula os conflitos do registro criando tabelas de conflito, que contêm as informações que devem ser colocadas na tabela se as alterações forem bem-sucedidas. Você pode examinar essas tabelas de conflitos e trabalhar nelas linha por linha, corrigindo o que for apropriado.

Todas as tabelas de conflito são\_chamadas de conflito de tabelas, onde table é o nome original da tabela, truncado para o comprimento máximo do nome da tabela.

