---
title: Comparação entre Microsoft Access SQL e ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd28cebe731ee3c922adec0bc3357e998dc1959b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463398"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Comparação entre Microsoft Access SQL e ANSI SQL


**Aplica-se a**: Access 2013 | Office 2013

O mecanismo de banco de dados Microsoft Access SQL é normalmente compatível com ANSI-89 Nível 1. Entretanto, certos recursos do ANSI SQL não são implementados no Microsoft® Access SQL. Em oposição, o Microsoft Access SQL inclui palavras reservadas e recursos não aceitos no ANSI SQL.

## <a name="major-differences"></a>Principais diferenças

  - O Microsoft Access SQL e o ANSI SQL têm diferentes palavras reservadas e tipos de dados. Para obter mais informações, consulte [Palavras reservadas SQL do mecanismo de banco de dados do Microsoft Access](sql-reserved-words.md) e [Tipos de dados ANSI SQL equivalentes](equivalent-ansi-sql-data-types.md). Utilizando o Provedor do OLE DB do mecanismo de banco de dados do Microsoft Access, há outras palavras reservadas.

  - **[Between…And](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**
    
    *expr1* \[Não\] **entre** *valor1* **e** *valor2*
    
    No Microsoft Access SQL, *value1* pode ser maior que *value2*; no ANSI SQL, *value1* deve ser igual ou menor que *value2.*

  - O Microsoft Access SQL fornece suporte a caracteres curinga do ANSI SQL e a [caracteres curinga](using-wildcard-characters-in-string-comparisons.md) específicos do mecanismo de banco de dados do Microsoft Access para serem usados com o operador **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**. O uso dos caracteres curinga do ANSI e do mecanismo de banco de dados do Microsoft Access é mutuamente exclusivo. Você deve usar um conjunto ou o outro e não é possível misturá-los. Os caracteres curinga do ANSI SQL estarão disponíveis somente ao utilizar o mecanismo de banco de dados do Microsoft Access e o Provedor OLE DB do mecanismo de banco de dados do Microsoft Access. Se você tentar usar os caracteres curinga do ANSI SQL no Microsoft Access ou no DAO, eles serão interpretados como literais. O oposto é verdadeiro, ao usar o Provedor OLE DB do mecanismo de banco de dados do Microsoft Access.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Correspondência de caracteres</p></th>
    <th><p>Microsoft Access SQL</p></th>
    <th><p>ANSI SQL</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Qualquer caractere simples</p></td>
    <td><p>?</p></td>
    <td><p>_ (sublinhado)</p></td>
    </tr>
    <tr class="even">
    <td><p>Zero ou mais caracteres</p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


  - O Microsoft Access SQL é geralmente menos restritivo. Por exemplo, ele permite agrupar e ordenar caracteres em expressões.

  - O Microsoft Access SQL fornece suporte a expressões mais poderosas.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Recursos avançados do Microsoft Access SQL

O Microsoft Access SQL fornece os seguintes recursos avançados:

  - A instrução [TRANSFORM](transform-statement-microsoft-access-sql.md), que fornece suporte para consultas de tabela de referência cruzada.

  - [Funções agregadas](sql-aggregate-functions-sql.md) adicionais, como **StDev** e **VarP**.

  - A declaração [PARAMETERS](parameters-declaration-microsoft-access-sql.md) para definição de consulta de parâmetro.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Recursos do ANSI SQL não aceitos no Microsoft Access SQL

O Microsoft Access SQL não fornece suporte ao seguintes recursos do ANSI SQL:

  - Referências à função de agregação DISTINCT. Por exemplo, o Microsoft Access SQL não permite SUM(DISTINCT *nome_da_coluna*).

  - A cláusula LIMIT TO *nn* ROWS usada para limitar o número de linhas retornadas por uma consulta. Você pode usar apenas a [cláusula WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) para limitar o escopo de uma consulta.
