---
title: Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d9dc28bd64966e85d16ee2d8cb62fdebc3ba942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296868"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Estes métodos de transação gerenciam o processamento das transações em um objeto [Connection](connection-object-ado.md) da seguinte forma:

- **BeginTrans**  inicia uma nova transação.

- **CommitTrans**  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.

- **RollbackTrans**  cancela qualquer alteração feita durante a transação atual e finaliza a transação. Também pode iniciar uma nova transação.

## <a name="syntax"></a>Sintaxe

*level*  =  *objeto*. BeginTrans()

*objeto*. BeginTrans

*objeto*. CommitTrans

*objeto*. RollbackTrans

## <a name="return-value"></a>Valor de retorno

**BeginTrans** pode ser chamado como uma função que retorna uma variável **Long**, que indica o nível de aninhamento da transação.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*objeto* |Um objeto **Connection**.|

### <a name="connection"></a>Connection

Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.

> [!NOTE]
> [!OBSERVAçãO] Nem todos os provedores oferecem suporte a transações. Verifique se a propriedade definida pelo provedor **Transaction DDL** aparece na coleção Properties do objeto [](properties-collection-ado.md) **Connection,** indicando que o provedor oferece suporte a transações. Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.

Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.

Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.

A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.

Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.

### <a name="remote-data-service"></a>Remote Data Service

Os métodos **BeginTrans**, **CommitTrans** e **RollbackTrans** não estão disponíveis em um objeto **Connection** do cliente.

