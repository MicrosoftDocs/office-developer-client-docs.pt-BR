---
title: Evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288473"
---
# <a name="onerror-event-rds"></a>Evento onError (RDS)

**Aplica-se ao:** Access 2013, Office 2013

O evento **onError** é chamado sempre que ocorre um erro durante uma operação.

## <a name="syntax"></a>Sintaxe

onError *SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*SCode* |Um número inteiro que indica o código de status do erro.|
|*Description* |Uma **Sequência** que indica uma descrição do erro.|
|*Source* |Uma **Sequência** que indica a consulta ou o comando que causou o erro.|
|*CancelDisplay* |Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.|

