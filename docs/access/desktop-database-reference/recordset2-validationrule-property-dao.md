---
title: Propriedade Recordset2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0c6df32c37f73dadf1df43201090d44d81a6a01
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890943"
---
# <a name="recordset2validationrule-property-dao"></a>Propriedade Recordset2.ValidationRule (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationRule

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

As configurações ou valores de retorno são um **String** que descreve uma comparação no formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade será leitura/gravação.

A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornada será o texto da propriedade **ValidationText**, se especificado, ou o texto da expressão especificada por **ValidationRule**.

Para um objeto **Recordset**, o uso da propriedade **ValidationRule** é somente leitura. Para um objeto **TableDef**, o uso da propriedade **ValidationRule** depende do status do objeto **TableDef**, como mostra a tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>TableDef</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tabela base</p></td>
<td><p>Leitura/gravação</p></td>
</tr>
<tr class="even">
<td><p>Tabela vinculada</p></td>
<td><p>Somente leitura</p></td>
</tr>
</tbody>
</table>


Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.

A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.

A propriedade **ValidationRule** de um objeto **Recordset** ou **TableDef** pode se referir a vários campos desse objeto. As restrições observadas anteriormente neste tópico do objeto **Field** são aplicáveis.

Para um **Recordset** do tipo tabela, a propriedade **ValidationRule** herda a definição de propriedade de **ValidationRule** do objeto **TableDef** usado para criar o objeto **Recordset** do tipo tabela.


> [!NOTE]
> <P>Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</P>


