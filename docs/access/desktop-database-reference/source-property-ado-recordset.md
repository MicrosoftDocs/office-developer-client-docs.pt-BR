---
title: Propriedade Source (Recordset do ADO)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306404"
---
# <a name="source-property-ado-recordset"></a>Propriedade Source (Recordset do ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica a fonte de dados de um objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define um valor **String** ou a referência de objeto [Command](command-object-ado.md); retorna somente um valor **String** que indica a origem do **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Source** para especificar uma fonte de dados para um objeto **Recordset** utilizando uma das seguintes opções: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado ou um nome de tabela.

Se você definir a propriedade **Source** para um objeto **Command**, a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Recordset** herdará o valor da propriedade **ActiveConnection** para o objeto **Command** especificado. Entretanto, a leitura da propriedade **Source** não retornará o objeto **Command**; em vez disso, retornará a propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** para o qual você definiu a propriedade **Source**.

Se a propriedade **Source** for uma instrução SQL, um procedimento armazenado ou um nome de tabela, será possível otimizar o desempenho enviando o argumento adequado *Options* com a chamada do método [Open](open-method-ado-recordset.md).

A propriedade **Source** é leitura/gravação para objetos **Recordset** fechados e somente leitura para objetos **Recordset** abertos.

