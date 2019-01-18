---
title: Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716030"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Métodos MoveFirst, MoveLast, MoveNext e MovePrevious (RDS)

**Aplica-se a**: Access 2013, o Office 2013

Move para o primeiro, o último, o próximo ou o registro anterior em um objeto [Recordset](recordset-object-ado.md) especificado.

## <a name="syntax"></a>Sintaxe

*DataControl*. Conjunto de registros. { Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentários

Você pode usar os métodos **Move** com o **RDS. DataControl** objeto para navegar pelos registros de dados nos controles ligados a dados em uma página da Web. 

Por exemplo, suponha que você exiba um **Recordset** em uma grade ligando a um objeto **RDS.DataControl**. Em seguida, é possível incluir botões Primeiro, Último, Próximo e Anterior que os usuários podem clicar para mover-se para o primeiro, o último, o próximo ou o registro anterior no **Recordset** exibido. Isso é feito chamando-se os métodos **MoveFirst**, **MoveLast**, **MoveNext** e **MovePrevious** do objeto **RDS.DataControl** nos procedimentos onClick dos botões Primeiro, Último, Próximo e Anterior, respectivamente. O [Exemplo de Catálogo de Endereços](address-book-navigation-buttons.md) mostra como fazer isso.

