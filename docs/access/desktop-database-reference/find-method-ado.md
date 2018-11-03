---
title: Localizar o método - ActiveX Data Objects (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ff66a39de070759e0ad31b441e4be5735d87516
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936606"
---
# <a name="find-method-ado"></a>Método Find (ADO)


**Aplica-se a**: Access 2013, o Office 2013


Procura um [Recordset](recordset-object-ado.md) para a linha que satisfaz os critérios especificados. Opcionalmente, a direção da pesquisa, a linha inicial e o deslocamento a partir da linha inicial podem ser especificados. Se os critérios forem atendidos, a posição da linha atual é definida no registro encontrado; caso contrário, a posição é definida para o final (ou início) do **Recordset**.

## <a name="syntax"></a>Sintaxe

Encontre (*critérios*, *SkipRows*, *SearchDirection*, *Iniciar*)

## <a name="parameters"></a>Parâmetros

  - *Criteria*

  - Um valor **String** que contém uma instrução que especifica o nome da coluna, o operador da comparação e o valor a ser utilizado na pesquisa.

  - *SkipRows*

  - Opcional *.* Um valor **Long**, cujo valor padrão é zero, que especifica o deslocamento de linha a partir da linha atual ou do indicador *Start* para iniciar a pesquisa. Por padrão, a pesquisa iniciará na linha atual.

  - *SearchDirection*

  - Opcional *.* Um valor [SearchDirectionEnum](searchdirectionenum.md) que especifica que a pesquisa deve iniciar na linha atual ou na próxima linha disponível na direção da pesquisa. Uma pesquisa sem êxito para no final do **Recordset** se o valor for **adSearchForward**. Uma pesquisa sem êxito para no início do **Recordset** se o valor for **adSearchBackward**.

  - *Start*

  - Opcional. Um indicador **Variant** que funciona como a posição inicial da pesquisa.

## <a name="remarks"></a>Comentários

Apenas um único nome de coluna pode ser especificado em *criteria*. Este método não suporta pesquisas de várias colunas.

O operador de comparação nos *critérios* pode ser "**\>**"(maior que),"**\<**"(menor que), "=" (igual a),"\>=" (maior que ou igual), "\<=" (menor ou igual), "\<\>" (não igual a), ou "como" (padrão correspondente).

O valor nos *critérios* pode ser uma cadeia de caracteres, número de ponto flutuante ou data. Valores de cadeia de caracteres são delimitados por aspas simples ou "\#" (sinal numérico) marca (por exemplo, "estado = 'WA'" ou "estado = \#WA\#"). Valores de data são delimitados por "\#" (sinal numérico) marca (por exemplo, "Iniciar\_data \> \#22/7/97\#") e pode conter horas, minutos e segundos para indicar carimbos de tempo, mas não devem conter milissegundos ou ocorrerão erros .

Se o operador de comparação for "like", o valor da sequência poderá conter um asterisco (\*) para localizar uma ou mais ocorrências de qualquer caractere ou subsequência. Por exemplo, "state like 'M\*'" corresponde a Maine e Massachusetts. Também é possível utilizar asteriscos à esquerda e à direita para localizar uma subsequência contida nos valores. Por exemplo, "state like '\*as\*'" corresponde a Alaska, Arkansas e Massachusetts.

Os asteriscos podem ser utilizados apenas no final de uma sequência de critérios ou em conjunto, tanto no início quanto no final de uma sequência de critérios, conforme mostrado acima. Não é possível utilizar o asterisco como um caractere curinga inicial ('\*str') ou como caractere curinga incorporado ('s\*r'). Isso causará um erro.


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro se uma posição de linha atual não for definida antes de chamar **Find**. Qualquer método que defina posição de linha, tal como [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), deve ser chamado antes de chamar **Find**.

> [!NOTE]
> [!OBSERVAçãO] Se você chamar o método **Find** em um recordset e a posição atual no recordset estiver no último registro ou no final do arquivo (EOF), nada será encontrado. É necessário chamar o método **MoveFirst** para definir a posição atual/cursor para o início do recordset.


