---
title: Método CancelUpdate (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28216cbeb98a0ebc7dfbc6115ea8bc05fadc057f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887744"
---
# <a name="cancelupdate-method-rds"></a>Método CancelUpdate (RDS)


**Aplica-se a**: Access 2013, o Office 2013



Cancela quaisquer alterações feitas na linha atual ou nova de um objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxe

*DataControl*. CancelUpdate

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

## <a name="remarks"></a>Comentários

O Cursor Service for OLE DB mantém uma cópia dos valores originais e um cache de alterações. Ao chamar **CancelUpdate**, o cache de alterações é redefinido para vazio e quaisquer controles de ligação são atualizados com os dados originais.

