---
title: Evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a61ec584f5baddcfdb8ce1f6dda1bf990546c053
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949352"
---
# <a name="onerror-event-rds"></a>Evento onError (RDS)

**Aplica-se a**: Access 2013, o Office 2013

O evento **onError** é chamado sempre que ocorre um erro durante uma operação.

## <a name="syntax"></a>Sintaxe

AoOcorrerErro*SCode*, *Descrição*, *fonte*, *CancelDisplay*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*SCode* |Um número inteiro que indica o código de status do erro.|
|*Description* |Uma **Sequência** que indica uma descrição do erro.|
|*Source* |Uma **Sequência** que indica a consulta ou o comando que causou o erro.|
|*CancelDisplay* |Um valor **booleano**, que, se for definido como **Verdadeiro**, impede que o erro seja exibido em uma caixa de diálogo.|

