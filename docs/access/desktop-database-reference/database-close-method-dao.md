---
title: Método Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699967"
---
# <a name="databaseclose-method-dao"></a>Método Database.Close (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Fecha um objeto **Database** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* . Fechar

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="remarks"></a>Comentários

Se o objeto **Database** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.

Uma alternativa ao método **Close** é definir o valor de uma variável de objeto para **Nothing** (Set dbsTemp = Nothing).

