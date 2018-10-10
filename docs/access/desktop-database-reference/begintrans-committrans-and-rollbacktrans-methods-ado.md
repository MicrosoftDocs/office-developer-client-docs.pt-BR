---
title: Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69d3d7830204ec400e01b64bb11434c272da5c29
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463214"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Estes métodos de transação gerenciam o processamento das transações em um objeto [Connection](connection-object-ado.md) da seguinte forma:

  - **BeginTrans**  inicia uma nova transação.

  - **CommitTrans**  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.

  - **RollbackTrans**  cancela qualquer alteração feita durante a transação atual e finaliza a transação. Também pode iniciar uma nova transação.

## <a name="syntax"></a>Sintaxe

*nível* = *objeto*. BeginTrans()

*objeto*. BeginTrans

*objeto*. CommitTrans

*objeto*. RollbackTrans

## <a name="return-value"></a>Valor de retorno

**BeginTrans** pode ser chamado como uma função que retorna uma variável **Long**, que indica o nível de aninhamento da transação.

## <a name="parameters"></a>Parâmetros

  - *object*

  - Um objeto **Connection**.

**Objeto Connection**

Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.


> [!NOTE]
> <P>Nem todos os provedores oferecem suporte a transações. Verifique se a propriedade "<STRONG>Transaction DDL</STRONG>" definida pelo provedor aparece na coleção <A href="properties-collection-ado.md">Properties</A> do objeto <STRONG>Connection</STRONG>, indicando o suporte do provedor a transações. Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.</P>



Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.

Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.

A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.

Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.

**Remote Data Service**

Os métodos **BeginTrans**, **CommitTrans** e **RollbackTrans** não estão disponíveis em um objeto **Connection** do cliente.

