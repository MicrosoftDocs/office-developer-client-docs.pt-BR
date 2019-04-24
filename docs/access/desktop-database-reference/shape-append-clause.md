---
title: Cláusula Shape Append
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306444"
---
# <a name="shape-append-clause"></a>Cláusula Shape Append


**Aplica-se ao:** Access 2013, Office 2013

A cláusula APPEND do comando shape acrescenta uma ou mais colunas a um **Recordset**. Em geral, essas colunas referem-se a capítulos, que se referem a um **Recordset** filho .

## <a name="syntax"></a>Sintaxe

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Descrição

As partes dessa cláusula são as seguintes:

- *parent-command*

- Zero ou um dos itens a seguir (você pode omitir *parent-command* completamente):
    
  - Um comando de provedor entre chaves ("{}") que retorna um objeto **Recordset**. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.
    
  - Um outro comando shape entre parênteses.
    
  - A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.

- *parent-alias*

  - Um alias opcional que se refere ao **Recordset** pai.

- *column-list*

  - Um ou mais itens a seguir:
    
    - Uma coluna agregada.
    
    - Uma coluna calculada.
    
    - Uma nova coluna criada com a cláusula NEW.
    
    - Uma coluna de capítulo. Uma definição dessa coluna é exibida entre parênteses ("()"). Consulte a sintaxe a seguir:


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- *child-recordset*

  - Um comando de provedor entre chaves ("{}") que retorna um objeto **Recordset**. O comando é emitido para o provedor de dados subjacente, e sua sintaxe depende dos requisitos desse provedor. Em geral, será usada a linguagem SQL, embora o ADO não exija nenhuma linguagem de consulta específica.
    
  - Um outro comando shape entre parênteses.
    
  - O nome de um **Recordset** com formato existente.
    
  - A palavra-chave TABLE, seguida do nome de uma tabela no provedor de dados.

- *child-alias*

  - Um alias que se refere ao **Recordset** filho.

- *parent-column*

  - Uma coluna em **Recordset** retornada por *parent-command.*

- *child-column*

  - Uma coluna em **Recordset** retornada por *child-command.*

- *param-number*

  - Consulte [Operação dos comandos com parâmetros](operation-of-parameterized-commands.md).

- *chapter-alias*

  - Um alias que se refere à coluna de capítulo acrescentada ao pai.


> [!NOTE]
> - A cláusula _"Parent-Column to Child-Column"_ na verdade é uma lista, onde cada relação definida é separada por uma vírgula.
> - A cláusula após a palavra-chave APPEND na verdade é uma lista, na qual cada cláusula é separada por uma vírgula e define uma outra coluna a ser acrescentada ao pai.



## <a name="remarks"></a>Comentários

Quando você construir os comandos de provedor a partir da entrada do usuário como parte de um comando SHAPE, SHAPE tratará o comando de provedor fornecido pelo usuário como uma sequência opaca e o passará fielmente ao provedor. Por exemplo, no comando SHAPE a seguir,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

A forma executará dois comandos: \* selecione de T1 e ( \* selecione de T2 relacionar K1 para K2). Se o usuário emitir um comando composto contendo vários comandos de provedor separados por ponto-e-vírgula, SHAPE não conseguirá diferenciar. Portanto, no comando SHAPE a seguir,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

A forma executa Select \* from T1; descartar tabela T1 e \* (selecione de T2 relacionar K1 para K2), não percebendo que a tabela de descarte T1 é separada e, nesse caso, um comando de provedor perigoso. Os aplicativos devem sempre validar a entrada do usuário para impedir possíveis ataques de hacker como esse.

Esta seção inclui os seguintes tópicos:

- [Operação de comandos não parametrizados](operation-of-non-parameterized-commands.md)

- [Operação de comandos parametrizados](operation-of-parameterized-commands.md)

- [Comandos híbridos](hybrid-commands.md)

- [Cláusulas de cálculo da forma interveniente](intervening-shape-compute-clauses.md)
