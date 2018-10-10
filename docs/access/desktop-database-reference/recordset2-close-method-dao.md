---
title: Método Recordset2.Close (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f20c10ac6bb6fc313ffecb56b0d2852c3b488c26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464018"
---
# <a name="recordset2close-method-dao"></a>Método Recordset2.Close (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Fecha um **Recordset** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* . Fechar

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Se o objeto **Recordset** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.

Se você tentar fechar um objeto **Connection** enquanto ele tiver objetos **Recordset** abertos, os objetos **Recordset** serão fechados e quaisquer atualizações ou edições pendentes serão canceladas. Da mesma maneira, se você tentar fechar um objeto **Workspace** enquanto ele tiver objetos **Connection** abertos, esses objetos **Connection** serão fechados, o que fechará seus objetos **Recordset**.

Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).

