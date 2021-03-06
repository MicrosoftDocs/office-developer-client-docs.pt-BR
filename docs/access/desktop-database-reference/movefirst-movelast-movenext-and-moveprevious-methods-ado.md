---
title: Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cb6ea7f82ac37460d7f2a4dd998ae7435c04230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288782"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a>Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Move para o primeiro, o último, o próximo ou o registro anterior em um objeto [Recordset](recordset-object-ado.md) especificado e torna esse registro o atual.

## <a name="syntax"></a>Sintaxe

*recordset*. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="remarks"></a>Comentários

Utilize o método **MoveFirst** para mover a posição de registro atual para o primeiro registro no **Recordset**.

Utilize o método **MoveLast** para mover a posição de registro atual para o último registro no **Recordset**. O objeto **Recordset** deve suportar indicadores ou movimentação do cursor para trás; caso contrário, a chamada ao método gerará um erro.

Uma chamada a **MoveFirst** ou **MoveLast** quando o **Recordset** estiver vazio ( **BOF** e **EOF** são True) gera um erro.

Utilize o método **MoveNext** para mover a posição de registro atual um registro para frente (em direção ao final do **Recordset**). Se o último registro for o registro atual e você chamar o método **MoveNext**, o ADO definirá o registro atual para a posição após o último registro no **Recordset** ([EOF](bof-eof-properties-ado.md) é **True**). Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.

Nos casos em que o **Recordset** foi filtrado ou classificado e os dados do registro atual forem alterados, a posição também pode ser alterada. Nesses casos, o método **MoveNext** funciona normalmente, mas você deve estar ciente de que a posição é movida um registro para a frente a partir da nova posição, não da posição antiga. Por exemplo, alterar os dados no registro atual, de forma que o registro seja movido para o final do **Recordset classificação,** significa que chamar **MoveNext** resulta na definição do registro atual do ADO para a posição após o último registro no **Recordset** (**EOF**  =  **True**).

Utilize o método **MovePrevious** para mover a posição de registro atual um registro para trás (em direção ao início do **Recordset**). O objeto **Recordset** deve suportar indicadores ou movimentação do cursor para trás; caso contrário, a chamada ao método gerará um erro. Se o primeiro registro for o registro atual e você chamar o método **MovePrevious**, o ADO definirá o registro atual para a posição antes do primeiro registro no **Recordset** ([BOF](bof-eof-properties-ado.md) é **True**). Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro. Se o objeto **Recordset** não suportar indicadores ou movimentação do cursor para trás, o método **MovePrevious** gerará um erro.

Se o **Recordset** for apenas de avanço e você deseja suportar rolagem para frente e para trás, poderá utilizar a propriedade [CacheSize](cachesize-property-ado.md) para criar um cache de registro que suportará movimentação do cursor para trás por meio do método [Move](move-method-ado.md). Como os registros em cache são carregados em memória, você deve evitar o armazenamento em cache de mais registros que o necessário. É possível chamar o método **MoveFirst** em um objeto **Recordset** apenas de avanço; isso pode fazer com que o provedor execute novamente o comando que gerou o objeto **Recordset**.

