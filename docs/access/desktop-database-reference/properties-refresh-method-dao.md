---
title: Método Properties.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4df20311746b562d319e371da3cf75b452c064e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462834"
---
# <a name="propertiesrefresh-method-dao"></a>Método Properties.Refresh (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizar

*expressão* Uma variável que representa um objeto **Properties** .

## <a name="remarks"></a>Comentários

Use o método **Refresh** em ambientes multiusuários nos quais outros usuários podem alterar o banco de dados. Talvez seja necessário usá-lo em coleções indiretamente afetadas por alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, talvez seja necessário atualizar uma coleção **Groups** antes de usar a coleção **Groups**.

Uma coleção é preenchida por objetos na primeira vez que se faz referência a ela e não refletirá automaticamente as alterações subsequentes que outros usuários fizerem. Se é provável que outro usuário tenha alterado a coleção, use o método Refresh na coleção imediatamente antes de realizar qualquer tarefa em seu aplicativo que pressuponha a presença ou a ausência de um objeto específico na coleção. Isso vai assegurar que a coleção esteja o mais atualizada possível. Paralelamente, o uso do Refresh pode reduzir o desempenho desnecessariamente.

