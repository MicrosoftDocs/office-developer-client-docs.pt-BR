---
title: Propriedade Recordset2. UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309068"
---
# <a name="recordset2updateoptions-property-dao"></a>Propriedade Recordset2. UpdateOptions (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . UpdateOptions

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Quando um modo de lote **[Update](recordset2-update-method-dao.md)** for executado, o DAO e a biblioteca de cursores em lotes do cliente criarão uma série de instruções SQL UPDATE para fazer as alterações necessárias. Uma cláusula SQL WHERE será criada para cada atualização com a finalidade de isolar os registros marcados como alterados pela propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)**. Como alguns servidores remotos usam gatilhos ou outras formas para forçar a integridade referencial, é importante limitar, com frequência, os campos que estão sendo atualizados para apenas aqueles afetados pela alteração. 

Para fazer isso, defina a propriedade **UpdateOptions** como uma das constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**. Dessa forma, será executada somente a quantidade mínima absoluta de um código do gatilho. Como resultado, a operação de atualização será executada de forma mais rápida e com menos erros potenciais.

Você também pode concatenar qualquer uma das constantes **dbCriteriaDeleteInsert** ou **dbCriteriaUpdate** para determinar se será necessário usar um conjunto de instruções SQL DELETE e INSERT ou uma instrução SQL UPDATE para cada atualização durante o envio das modificações em lotes de volta para o servidor. No caso anterior, foram necessárias duas operações separadas para atualizar o registro. Em alguns casos, especialmente naqueles em que o sistema remoto implementou os gatilhos DELETE, INSERT e UPDATE, a escolha da definição da propriedade **UpdateOptions** correta pode impactar, de forma significativa, o desempenho.

Se você não especificar nenhuma constante, serão usadas **dbCriteriaUpdate** e **dbCriteriaKey**.

Os registros recentemente adicionados sempre gerarão instruções INSERT e os registros excluídos sempre gerarão instruções DELETE, de modo que essa propriedade se aplicará somente na forma como a bibiloteca de cursores atualizará os registros modificados.

