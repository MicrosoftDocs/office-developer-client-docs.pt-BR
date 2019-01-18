---
title: Data shaping (referência de banco de dados da área de trabalho do Access)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad507ac8c963f1d6ead7bc3bf444e694d83f90e3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716807"
---
# <a name="data-shaping"></a>Data Shaping

**Aplica-se a**: Access 2013, o Office 2013

A forma dos dados permite definir as colunas de um **Recordset** formado, as relações entre as entidades representadas pelas colunas e a maneira na qual o **Recordset** é preenchido com dados.

As colunas de um **Recordset** formado podem conter dados de um provedor de dados como o Microsoft SQL Server, referência a outro **Recordset**, valores derivados de um cálculo em uma única linha de um **Recordset**, valores derivados de uma operação sobre uma coluna de um **Recordset** inteiro; ou pode ser uma coluna vazia recém-fabricada.

Ao recuperar o valor de uma coluna que contenha uma referência a outro **Recordset**, o ADO retorna automaticamente o **Recordset** real representado pela referência. Um **Recordset** que contém outro **Recordset** é chamado de conjunto de registro hierárquico. Os conjuntos de registro hierárquicos exibem uma relação *pai-filho*, no qual o *pai* é o conjunto de registro que contém e o *filho* é o conjunto de registro contido. A referência a um **Recordset** é, na realidade, uma referência a um subconjunto do filho, chamado de *capítulo*. Um único pai pode fazer referência a mais de um filho **Recordset**.

A sintaxe do comando shape permite criar programaticamente um **Recordset** formado. Em seguida, você pode acessar os componentes do **Recordset** programaticamente ou através de um controle visual apropriado. Um comando shape é emitido como qualquer outro texto de comando ADO.

Você pode tornar objetos **Recordset** hierárquicos de duas maneiras com a sintaxe do comando shape. A primeira anexa um **Recordset** filho a um **Recordset** pai. O pai e o filho geralmente possuem, no mínimo, uma coluna em comum: o valor da coluna em uma linha do pai tem o mesmo valor da coluna em todas as linhas do filho.

A segunda maneira gera um **Recordset** pai de um **Recordset** filho. Os registros no **Recordset** filho são agrupados, geralmente usando a cláusula BY e uma linha é adicionada ao **Recordset** pai para cada grupo resultante no filho. Se a cláusula BY for omitida, o **Recordset** filho formará um único grupo e o **Recordset** pai conterá exatamente uma linha. Isso é útil para calcular os agregados do "grand total" sobre o **Recordset** filho inteiro.

Independentemente do **Recordset** pai que é formado, isso conterá uma coluna de capítulo que é usado para relacioná-lo ao **Recordset** filho. Se você desejar, o **Recordset** também pode ter colunas que contenham agregados (SUM, MIN, MAX e assim por diante) sobre as linhas filho. Tanto o **Recordset** pai como o filho que contêm uma expressão na linha no **Recordset**, bem como colunas que sejam novas e inicialmente vazias.

Você pode aninhar objetos **Recordset** hierárquicos a qualquer profundidade (ou seja, criar objetos **Recordset** filho de objetos **Recordset** filho e assim por diante).

Você pode acessar os componentes **Recordset** do **Recordset** formado de forma programática ou através de um controle visual apropriado.

Para obter exemplos de comandos shape e suas hierarquias resultantes, consulte Usando o serviço de forma de dados para OLE DB: Uma visão geral melhor.

Esta seção inclui os seguintes tópicos:

- [Reformatação](reshaping.md)
- [Agregados netos](grandchild-aggregates.md)
- [Comandos parametrizados com comandos COMPUTE intermediários](parameterized-commands-with-intervening-compute-commands.md)
- [Mantendo Recordsets hierárquicos](persisting-hierarchical-recordsets.md)
