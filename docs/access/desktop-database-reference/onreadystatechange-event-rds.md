---
title: Evento onReadyStateChange (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869229"
---
# <a name="onreadystatechange-event-rds"></a>Evento onReadyStateChange (RDS)


**Aplica-se a**: Access 2013, o Office 2013


O evento **onReadyStateChange** é chamado sempre que o valor da propriedade [ReadyState](readystate-property-rds.md) é alterado.

## <a name="syntax"></a>Sintaxe

onReadyStateChange

## <a name="parameters"></a>Parâmetros

Nenhum.

## <a name="remarks"></a>Comentários

A propriedade **ReadyState** reflete o andamento de um objeto [RDS.DataControl](datacontrol-object-rds.md) uma vez que ele recupera, de maneira assíncrona, os dados em seu objeto [Recordset](recordset-object-ado.md). Use o evento **onReadyStateChange** para monitorar as alterações na propriedade **ReadyState** sempre que elas ocorrerem. Isso é mais eficiente do que verificar periodicamente o valor da propriedade.

