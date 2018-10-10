---
title: Propriedade TableDef.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d396c830ecaffd1f1c2d8d57f509baaa9171ae9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465438"
---
# <a name="tabledefvalidationrule-property-dao"></a>Propriedade TableDef.ValidationRule (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . ValidationRule

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

As configurações ou valores de retorno são um **String** que descreve uma comparação no formulário de uma cláusula SQL WHERE sem a palavra reservada WHERE. Para um objeto ainda não acrescentado à coleção **Fields**, essa propriedade será leitura/gravação.

A propriedade **ValidationRule** determina se um campo contém ou não dados válidos. Se os dados não forem válidos, ocorrerá um erro interceptável de tempo de execução. A mensagem de erro retornada será o texto da propriedade **ValidationText**, se especificado, ou o texto da expressão especificada por **ValidationRule**.

Somente há suporte para a validação em bancos de dados que usam o mecanismo do banco de dados do Microsoft Access.

A expressão da cadeia de caracteres especificada pela propriedade **ValidationRule** de um objeto **Field** pode se referir apenas a esse **Field** e não às funções definidas pelo usuário, às funções agregadas SQL ou às consultas. Para definir uma propriedade **ValidationRule** do objeto **Field** quando a definição da propriedade **ValidateOnSet** for **True**, a expressão deverá analisar com sucesso o nome do campo (com o nome do campo como um operando implícito) e avaliá-lo como **True**. Caso a definição da propriedade **ValidateOnSet** seja **False**, a definição da propriedade **ValidationRule** será ignorada.

A propriedade **ValidationRule** de um objeto **Recordset** ou **TableDef** pode se referir a vários campos desse objeto. As restrições observadas anteriormente neste tópico do objeto **Field** são aplicáveis.

Para um objeto **TableDef** baseado em uma tabela vinculada, a propriedade **ValidationRule** herda a definição da propriedade **ValidationRule** da tabela base. Se a tabela base não oferecer suporte à validação, o valor dessa propriedade será uma sequência com comprimento zero ("").


> [!NOTE]
> <P>Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal de fora dos EUA, como uma vírgula (por exemplo, strRule = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro quando seu código tenta validar todos os dados. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.</P>


