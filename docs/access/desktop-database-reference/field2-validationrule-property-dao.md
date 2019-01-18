---
title: Propriedade Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713188"
---
# <a name="field2validationrule-property-dao"></a>Propriedade Field2.ValidationRule (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationRule

*expressão* Uma expressão que retorna um objeto **Field2** .

## <a name="remarks"></a>Comentários

As configurações ou os valores de retorno são uma String que descreve uma comparação em um formulário da cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade é de leitura/gravação.

A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro de tempo de execução interceptável. A mensagem de erro retornada é o texto da propriedade **ValidationText**, se especificada, ou o texto da expressão especificada por **ValidationRule**.

Para um objeto **Field2**, a utilização da propriedade **ValidationRule** depende do objeto que contém a coleção **Fields** à qual o objeto **Field2** foi acrescentado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto acrescentado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Índice</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relação</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>


Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.

A expressão de sequência especificada pela propriedade **ValidationRule** de um objeto **Field2** pode se referir apenas a **Field2**. A expressão não pode se referir às funções definidas pelo usuário, às funções agregadas SQL nem às consultas. Para definir a propriedade **ValidationRule** de um objeto **Field2**, quando a configuração de sua propriedade **ValidateOnSet** for **True**, a expressão deve ser analisada com sucesso (com o nome do campo como um operando implícito) e avaliada como **True**. Se a configuração de sua propriedade **ValidateOnSet** for **False**, a configuração da propriedade **ValidationRule** será ignorada.


> [!NOTE]
> Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados. Isso acontece porque durante a concatenação, o número será convertido para uma sequência que usa os caracteres decimais padrão do sistema e o mecanismo SQL do banco de dados do Microsoft Access aceita somente os caracteres decimais padrão dos EUA.


