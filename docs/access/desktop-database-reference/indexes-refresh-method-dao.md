---
title: Método Indexes.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: ffe1bc79-5a56-2a70-c5ac-2f80b683adbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837325(v=office.15)
ms:contentKeyID: 48548973
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7e1b2a017342532f3eba1e14ce6097fea8ebffa8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709366"
---
# <a name="indexesrefresh-method-dao"></a>Método Indexes.Refresh (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizar

*expressão* Uma variável que representa um objeto **Indexes** .

## <a name="remarks"></a>Comentários

Use o método **Refresh** em ambientes multiusuários nos quais outros usuários podem alterar o banco de dados. Talvez seja necessário usá-lo em coleções indiretamente afetadas por alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, talvez seja necessário atualizar uma coleção **Groups** antes de usar a coleção **Groups**.

Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.

