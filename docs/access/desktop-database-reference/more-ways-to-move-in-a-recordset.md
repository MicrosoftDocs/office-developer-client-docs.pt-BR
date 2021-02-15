---
title: Outras formas de movimentação em um conjunto de registros
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d10a493aac39934a047c6fa311233fd6c9fac4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288859"
---
# <a name="more-ways-to-move-in-a-recordset"></a>Outras formas de movimentação em um conjunto de registros

**Aplica-se ao:** Access 2013, Office 2013

Os seguintes métodos são usados para se mover em torno de ou para rolar em um objeto **Recordset**: [MoveFirst, MoveLast, MoveNext e MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md). (Alguns desses métodos não estão disponíveis em cursores apenas de avanço.)

**MoveFirst** transfere a posição de registro atual para o primeiro registro no **Recordset**. **MoveLast** transfere a posição de registro atual para o último registro no **Recordset**. Para usar **MoveFirst** ou **MoveLast**, o objeto **Recordset** deve oferecer suporte a marcadores ou a movimentação de cursor para trás; caso contrário, o método gerará um erro.

**MoveNext** move o registro atual uma posição para frente. Se você estiver no último registro quando chamar **MoveNext**, **EOF** será definida como **True**. **MovePrevious** move o registro atual uma posição para trás. Se você estiver no primeiro registro quando chamar **MovePrevious**, **BOF** será definida como **True**. É recomendável verificar as propriedades **EOF** e **BOF** ao usar esses métodos e mover o cursor para trás até uma posição de registro atual válida caso se mova para fora de do **Recordset**, conforme mostrado aqui:

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

Ou, no caso do método **MovePrevious**:

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

Nos casos em que o **Recordset** foi filtrado ou classificado e os dados do registro atual forem alterados, a posição também pode ser alterada. Nesses casos, o método **MoveNext** funciona normalmente, mas esteja ciente de que a posição é movida um registro para a frente a partir da nova posição, não da posição antiga. Por exemplo, alterar os dados no registro atual, de forma que o registro seja movido para o final do **Recordset** classificação, significa que chamar **MoveNext** resulta na definição do registro atual do ADO para a posição após o último registro no **Recordset** (**EOF**  =  **True**).

O comportamento de vários métodos Move do objeto **Recordset** depende, de alguma forma, dos dados no **Recordset**. Os novos registros adicionados ao **Recordset** são inicialmente adicionados em uma ordem específica, que é definida pela fonte de dados e pode ser dependente, de forma implícita ou explícita, dos dados no novo registro. Por exemplo, se uma classificação ou junção for feita dentro da consulta que popula o **Recordset**, o novo registro será inserido no local apropriado dentro do **Recordset**. Se a ordem não estiver especificada de forma clara na criação do **Recordset**, as alterações na implementação da fonte de dados podem modificar a ordem das linhas retornadas inadvertidamente. Além disso, as funções de classificação, filtragem e edição do **Recordset** podem afetar a ordem e possivelmente a visibilidade de algumas linhas no Recordset.

Portanto, **MoveNext**, **MovePrevious**, **MoveFirst**, **MoveLast** e **Move** são todos afetados por outras operações executadas no mesmo **Recordset**. O ADO sempre tentará manter sua posição atual até que você explicitamente mova-o, mas algumas vezes essas interferências dificultam o entendimento dos efeitos de uma movimentação subsequente. Por exemplo, se chamar **MoveFirst** para uma posição na primeira linha de um **Recordset** classificado da forma crescente para a decrescente, você ainda estará na mesma linha  mas agora ela será a última linha no **Recordset**. **MoveFirst** o levará a uma linha diferente (a nova primeira linha).

Como outro exemplo, se estiver posicionado em uma linha específica no meio de um **Recordset** e chamar **Delete** e, em seguida, chamar **MoveNext**, você agora estará posicionado no registro seguinte ao registro excluído. Mas chamar **MovePrevious** torna o registro anterior ao excluído o registro atual, porque o registro excluído não é mais contado na associação ativa do **Recordset**.

É especialmente difícil definir de forma consistente a semântica de movimentação pelos provedores de métodos que se movem de forma relativa ao registro atual — **MovePrevious**, **MoveNext** e **Move** — diante da alteração de dados no registro atual. Por exemplo, se você estiver trabalhando com um **Recordset** e alterar os dados no registro atual de forma que ele preceda todos os outros registros, mas os dados alterados não mais corresponderem ao filtro, não fica muito claro onde uma operação **MoveNext** poderá levá-lo. A conclusão mais segura é que o movimento relativo dentro do **Recordset** é mais arriscado do que o movimento absoluto (como usar **MoveFirst** ou **MoveLast**) quando os dados estiverem sendo modificados enquanto os registros forem editados, adicionados ou excluídos. A classificação e a filtragem devem ter como base a identificação ou a chave primária, porque esse tipo de valor não deve ser alterado.

