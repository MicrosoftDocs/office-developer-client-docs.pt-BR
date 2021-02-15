---
title: Método Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305954"
---
# <a name="workspaceclose-method-dao"></a>Método Workspace.Close (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Fecha um **Workspace** aberto.

## <a name="syntax"></a>Sintaxe

*expressão* .Close

*expressão* Uma variável que representa um objeto **Workspace**.

## <a name="remarks"></a>Comentários

Se o objeto **Workspace** já estiver fechado quando você usar **Close**, ocorrerá um erro de tempo de execução.

Uma alternativa ao método **Fechar**, é definir o valor de uma variável de um objeto para **Nada** (Definir dbsTemp = Nada).

