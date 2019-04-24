---
title: Método Find-ActiveX Data Objects (ADO)
TOCTitle: Find method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32f14e4aeed669e68d976559932306c3cb76c696
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292409"
---
# <a name="find-method-ado"></a>Método Find (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Procura um [Recordset](recordset-object-ado.md) para a linha que satisfaz os critérios especificados. Opcionalmente, a direção da pesquisa, a linha inicial e o deslocamento a partir da linha inicial podem ser especificados. Se os critérios forem atendidos, a posição da linha atual é definida no registro encontrado; caso contrário, a posição é definida para o final (ou início) do **Recordset**.

## <a name="syntax"></a>Sintaxe

Localizar (*critérios*, *SkipRows*, *SearchDirection*, *início*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Criteria* |Um valor **String** que contém uma instrução que especifica o nome da coluna, o operador da comparação e o valor a ser utilizado na pesquisa.|
|*SkipRows* |Opcional. Um valor **Long**, cujo valor padrão é zero, que especifica o deslocamento de linha a partir da linha atual ou do indicador *Start* para iniciar a pesquisa. Por padrão, a pesquisa iniciará na linha atual.|
|*SearchDirection* |Opcional. Um valor [SearchDirectionEnum](searchdirectionenum.md) que especifica que a pesquisa deve iniciar na linha atual ou na próxima linha disponível na direção da pesquisa. Uma pesquisa sem êxito para no final do **Recordset** se o valor for **adSearchForward**. Uma pesquisa sem êxito para no início do **Recordset** se o valor for **adSearchBackward**.|
|*Start* |Opcional. Um indicador **Variant** que funciona como a posição inicial da pesquisa.|

## <a name="remarks"></a>Comentários

Apenas um único nome de coluna pode ser especificado em *criteria*. Este método não suporta pesquisas de várias colunas.

O operador de comparação nos *critérios* pode ser**\>**"" (maior que),**\<**"" (menor que), "=" (igual),\>"=" (maior que ou igual),\<"=" (menor ou igual), "\<\>" (diferente) ou "Like" (correspondência de padrão).

O valor em *Criteria* pode ser uma sequência, um número de ponto flutuante ou uma data. Valores de cadeia de caracteres são delimitados por\#aspas simples ou marcas "" (sinal de número) (por exemplo, "State = ' wa ' \#"\#ou "state = WA"). os valores de data são\#delimitados com marcas "" (sinal de número) (por\_exemplo \> \#,\#"data de início 7/22/97") e podem conter horas, minutos e segundos para indicar carimbos de data/hora, mas não devem conter milissegundos ou erros ocorrerão .

Se o operador de comparação for "like", o valor da sequência poderá conter um asterisco (\*) para localizar uma ou mais ocorrências de qualquer caractere ou subsequência. Por exemplo, "state like 'M\*'" corresponde a Maine e Massachusetts. Também é possível utilizar asteriscos à esquerda e à direita para localizar uma subsequência contida nos valores. Por exemplo, "state like '\*as\*'" corresponde a Alaska, Arkansas e Massachusetts.

Os asteriscos podem ser utilizados apenas no final de uma sequência de critérios ou em conjunto, tanto no início quanto no final de uma sequência de critérios, conforme mostrado acima. Não é possível utilizar o asterisco como um caractere curinga inicial ('\*str') ou como caractere curinga incorporado ('s\*r'). Isso causará um erro.

> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro se uma posição de linha atual não for definida antes de chamar **Find**. Qualquer método que defina posição de linha, tal como [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), deve ser chamado antes de chamar **Find**.

> [!NOTE]
> [!OBSERVAçãO] Se você chamar o método **Find** em um recordset e a posição atual no recordset estiver no último registro ou no final do arquivo (EOF), nada será encontrado. É necessário chamar o método **MoveFirst** para definir a posição atual/cursor para o início do recordset.


