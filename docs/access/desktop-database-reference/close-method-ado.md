---
title: Método Close - ActiveX Data Objects (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296308"
---
# <a name="close-method-ado"></a>Método Close (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Fecha um objeto aberto e quaisquer objetos dependentes.

## <a name="syntax"></a>Sintaxe

*objeto*. Fechar

## <a name="remarks"></a>Comentários

Utilize o método **Close** para fechar um objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) ou [Stream](stream-object-ado.md) e liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, de definida a variável de objeto como *Nothing* (no Visual Basic) depois de fechar o objeto.

**Connection**

A utilização do método **Close** para fechar um objeto **Connection** também fecha quaisquer objetos **Recordset** ativos associados à conexão. Um objeto [Command](command-object-ado.md) associado ao objeto **Connection** que está sendo fechado persistirá, mas não mais estará associado a um objeto **Connection**; isto é, sua propriedade [ActiveConnection](activeconnection-property-ado.md) será definida como **Nothing**. Além disso, a coleção **Parameters** do objeto [Command](parameters-collection-ado.md) será limpa de quaisquer parâmetros definidos pelo provedor.

Posteriormente será possível chamar o método [Open](open-method-ado-connection.md) para restabelecer a conexão à mesma, ou outra, fonte de dados. Enquanto o objeto **Connection** está fechado, chamar quaisquer métodos que requeiram uma conexão aberta à fonte de dados gera um erro.

Fechar um objeto **Connection** enquanto existem objetos **Recordset** abertos na conexão reverte quaisquer alterações pendentes em todos os objetos **Recordset**. Fechar de forma explícita um objeto **Connection** (chamando o método **Close** ) enquanto uma transação está em andamento gera um erro. Se um objeto **Connection** ficar fora do escopo enquanto uma transação estiver em andamento, o ADO reverterá automaticamente a transação.

**Recordset, Record, Stream**

A utilização do método **Close** para fechar um objeto **Recordset**, **Record** ou **Stream** libera os dados associados e qualquer acesso exclusivo que possa ter existido aos dados por meio desse objeto específico. Posteriormente, é possível chamar o método [Open](open-method-ado-recordset.md) para reabrir o objeto com os mesmos atributos (ou modificados).

Enquanto um objeto **Recordset** está fechado, chamar quaisquer métodos que requeiram um cursor dinâmico gera um erro.

Se uma edição estiver em andamento durante o modo de atualização imediata, chamar o método **Close** gera um erro; em vez disso, chame primeiramente o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md). Se você fechar o objeto **Recordset** durante o modo de atualização em batch, todas as alterações desde a última chamada a [UpdateBatch](updatebatch-method-ado.md) serão perdidas.

Se você utilizar o método [Clone](clone-method-ado.md) para criar cópias de um objeto **Recordset** aberto, fechar o original ou um clone não afetará nenhuma das demais cópias.

