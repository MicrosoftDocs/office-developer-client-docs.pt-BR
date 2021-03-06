---
title: Seção SQL do arquivo de personalização
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295132"
---
# <a name="customization-file-sql-section"></a>Seção SQL do arquivo de personalização


**Aplica-se ao:** Access 2013, Office 2013

A seção **sql** pode conter uma nova sequência de caracteres SQL que substitui a sequência de comando do cliente. Se a seção não tiver nenhuma sequência de caracteres SQL, ela será ignorada.

A nova sequência de caracteres SQL pode conter parâmetros. Isso significa que os parâmetros na sequência de caracteres SQL da seção **sql** (designada pelo caractere '?') podem ser substituídos pelos argumentos correspondentes em um *identifier* na sequência de comando do cliente (designada por uma lista delimitada por vírgula entre parênteses). O identificador e a lista de argumentos funcionam como uma chamada de função.

Por exemplo, suponha que a cadeia de comando do cliente seja "CustomerByID(4)" , o header da seção SQL seja SQL CustomerByID e a nova cadeia de caracteres da seção SQL seja \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?". O manipulador gerará , o header da seção SQL é SQL CustomerByID e a nova cadeia de caracteres de seção SQL é \[ \] "SELECT \* FROM Customers WHERE CustomerID = ?". O manipulador gerará "SELECT FROM Customers WHERE CustomerID = 4" e usará essa cadeia de caracteres \* para consultar a fonte de dados.

Se a nova sequência de caracteres SQL for a sequência nula (""), a seção será ignorada.

Se a nova sequência de caracteres SQL for inválida, a execução da instrução não ocorrerá e o parâmetro cliente será efetivamente ignorado. Você pode executar esse procedimento de forma intencional para "desativar" todos os comandos SQL de cliente especificando:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Sintaxe

Uma entrada de sequência de caracteres SQL de substituição tem este formato:

**SQL=*sqlString***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sair</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL</strong></p></td>
<td><p>Uma sequência literal que indica uma entrada de seção SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Uma sequência de caracteres SQL que substitui a sequência de caracteres do cliente.</p></td>
</tr>
</tbody>
</table>

