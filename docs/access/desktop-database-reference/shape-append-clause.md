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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726348"
---
# <a name="shape-append-clause"></a>Cláusula Shape Append


**Aplica-se a**: Access 2013, o Office 2013

A cláusula APPEND do comando shape acrescenta uma ou mais colunas a um **Recordset**. Em geral, essas colunas referem-se a capítulos, que se referem a um **Recordset** filho .

## <a name="syntax"></a>Sintaxe

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a>Descrição

As partes dessa cláusula são as seguintes:

- *parent-command*

- Zero ou uma das opções a seguir (você pode omitir o *parent-command* completamente):
    
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

  - Uma coluna em **Recordset** retornada pelo *parent-command.*

- *child-column*

  - Uma coluna em **Recordset** retornada por *child-command.*

- *param-number*

  - Consulte [Operação dos comandos com parâmetros](operation-of-parameterized-commands.md).

- *chapter-alias*

  - Um alias que se refere à coluna de capítulo acrescentada ao pai.


> [!NOTE]
> - A cláusula _"parent-column TO filho-column"_ na verdade é uma lista, onde cada relação definida é separada por uma vírgula.
> - [!OBSERVAçãO] A cláusula após a palavra-chave APPEND na verdade é uma lista, na qual cada cláusula é separada por uma vírgula e define uma outra coluna a ser acrescentada ao pai.



## <a name="remarks"></a>Comentários

Quando você construir os comandos de provedor a partir da entrada do usuário como parte de um comando SHAPE, SHAPE tratará o comando de provedor fornecido pelo usuário como uma sequência opaca e o passará fielmente ao provedor. Por exemplo, no comando SHAPE a seguir,

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

FORMA irá executar dois comandos: selecione \* de t1 e (selecione \* do t2 relacionar k1 para k2). Se o usuário emitir um comando composto contendo vários comandos de provedor separados por ponto-e-vírgula, SHAPE não conseguirá diferenciar. Portanto, no comando SHAPE a seguir,

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

Executa de forma selecionar \* de t1; Descartar tabela t1 e (selecione \* do t2 relacionar k1 para k2), não percebendo que t1 da tabela de recebimento é uma separado e neste comando perigoso, caso, o provedor. Os aplicativos devem sempre validar a entrada do usuário para impedir possíveis ataques de hacker como esse.

Esta seção inclui os seguintes tópicos:

- [Operação dos comandos sem parâmetros](operation-of-non-parameterized-commands.md)

- [Operação dos comandos parametrizados](operation-of-parameterized-commands.md)

- [Comandos híbridos](hybrid-commands.md)

- [Cláusulas COMPUTE de intervenção de forma](intervening-shape-compute-clauses.md)
