---
title: Evento onReadyStateChange (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464148"
---
# <a name="onreadystatechange-event-rds"></a>Evento onReadyStateChange (RDS)


**Aplica-se a**: Access 2013 | Office 2013


O evento **onReadyStateChange** é chamado sempre que o valor da propriedade [ReadyState](readystate-property-rds.md) é alterado.

## <a name="syntax"></a>Sintaxe

onReadyStateChange

## <a name="parameters"></a>Parâmetros

Nenhum.

## <a name="remarks"></a>Comentários

A propriedade **ReadyState** reflete o andamento de um objeto [RDS.DataControl](datacontrol-object-rds.md) uma vez que ele recupera, de maneira assíncrona, os dados em seu objeto [Recordset](recordset-object-ado.md). Use o evento **onReadyStateChange** para monitorar as alterações na propriedade **ReadyState** sempre que elas ocorrerem. Isso é mais eficiente do que verificar periodicamente o valor da propriedade.

