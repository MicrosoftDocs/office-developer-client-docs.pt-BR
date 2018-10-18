---
title: Propriedade Source (Recordset do ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605258"
---
# <a name="source-property-ado-recordset"></a>Propriedade Source (Recordset do ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica a fonte de dados de um objeto [Recordset](recordset-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define um valor **String** ou a referência de objeto [Command](command-object-ado.md); retorna somente um valor **String** que indica a origem do **Recordset**.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Source** para especificar uma fonte de dados para um objeto **Recordset** utilizando uma das seguintes opções: uma variável de objeto **Command**, uma instrução SQL, um procedimento armazenado ou um nome de tabela.

Se você definir a propriedade **Source** para um objeto **Command**, a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Recordset** herdará o valor da propriedade **ActiveConnection** para o objeto **Command** especificado. Entretanto, a leitura da propriedade **Source** não retornará o objeto **Command**; em vez disso, retornará a propriedade [CommandText](commandtext-property-ado.md) do objeto **Command** para o qual você definiu a propriedade **Source**.

Se a propriedade **Source** é uma instrução SQL, um procedimento armazenado ou um nome de tabela, você pode otimizar o desempenho, passando o argumento adequado *Options* com a chamada do método [Open](open-method-ado-recordset.md) .

A propriedade **Source** é leitura/gravação para objetos **Recordset** fechados e somente leitura para objetos **Recordset** abertos.

