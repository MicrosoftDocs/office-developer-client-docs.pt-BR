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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295020"
---
# <a name="databaseclose-method-dao"></a>Método Database.Close (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Fecha um objeto **Database** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* .Close

*expressão* Uma variável que representa um objeto do **Banco de dados**.

## <a name="remarks"></a>Comentários

Se o objeto **Database** já estiver fechado quando você usar **Close**, ocorrerá um erro em tempo de execução.

Uma alternativa ao método **Fechar**, é definir o valor de uma variável de um objeto para **Nada** (Definir dbsTemp = Nada).

