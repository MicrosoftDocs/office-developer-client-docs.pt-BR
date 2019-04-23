---
title: Método paraMeters. Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 47db1602-e223-985d-881c-b73e2d26acb7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193228(v=office.15)
ms:contentKeyID: 48544607
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29374baf16ec6c296f869b6bbf17bfb153d21bb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287773"
---
# <a name="parametersrefresh-method-dao"></a>Método paraMeters. Refresh (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Atualiza os objetos na coleta especificada para refletir o esquema atual do banco de dados.

## <a name="syntax"></a>Sintaxe

*expressão* . Atualizado

*expressão* Uma variável que representa um **** objeto Parameters.

## <a name="remarks"></a>Comentários

Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.

Uma coleção é preenchida com objetos quando ela se refere, pela primeira vez, a e não reflete automaticamente as alterações subsequentes feitas por outros usuários. Se provavelmente outro usuário alterou uma coleção, use o método Refresh na coleção imediatamente antes de executar qualquer tarefa no aplicativo que considera a presença ou a ausência de um objeto particular na coleção. Isso garante que a coleção seja atualizada assim que possível. Por outro lado, utilizar Refresh pode desnecessariamente reduzir o desempenho.

