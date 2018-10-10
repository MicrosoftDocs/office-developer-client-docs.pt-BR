---
title: Método Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 266d80aae875ff8d3caf6cc2a5b742abf780172c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464035"
---
# <a name="connectionclose-method-dao"></a>Método Close (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Fecha um objeto **Connection** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* . Fechar

*expressão* Uma variável que representa um objeto de **Conexão** .

## <a name="remarks"></a>Comentários

Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.

Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.

Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).

