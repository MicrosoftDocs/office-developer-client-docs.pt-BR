---
title: Propriedade Field.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a737f19b33777ea9c3acaf3bc6a9de5144a4db6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874073"
---
# <a name="fieldvalidationrule-property-dao"></a>Propriedade Field.ValidationRule (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationRule

*expressão* Uma expressão que retorna um objeto **Field** .

## <a name="remarks"></a>Comentários

As configurações ou os valores de retorno são um String que descreve uma comparação em um formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **[Fields](fields-collection-dao.md)**, essa propriedade será leitura/gravação.

A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornado será o texto da propriedade **[ValidationText](field-validationtext-property-dao.md)**, se especificado, ou o texto da expressão especificada por **ValidationRule**.

Para um objeto **[Field](field-object-dao.md)**, o uso da propriedade **ValidationRule** depende do objeto que contém a coleção **Fields** na qual o objeto **Field** foi acrescentado.

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

A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.


> [!NOTE]
> <P>Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados. Isso acontece porque durante a concatenação, o número será convertido para uma sequência que usa os caracteres decimais padrão do sistema e o mecanismo SQL do banco de dados do Microsoft Access aceita somente os caracteres decimais padrão dos EUA.</P>


