---
title: Processamento de transação
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13f25df31bea1eb742b4a7e7c958ccdbfb7274a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703339"
---
# <a name="transaction-processing"></a>Processamento de transações

**Aplica-se a**: Access 2013, o Office 2013

O ADO fornece os seguintes métodos para controlar transações: **BeginTrans**, **CommitTrans** e **RollbackTrans**. Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.

> [!NOTE]
> Nem todos os provedores oferecem suporte a transações. Verifique se a propriedade "**Transaction DDL**" definida pelo provedor aparece na coleção [Properties](properties-collection-ado.md) do objeto **Connection**, indicando o suporte do provedor a transações. Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.

Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.

A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.

Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.

## <a name="transaction-isolation-level"></a>Nível de isolamento da transação

Use a propriedade **IsolationLevel** para definir o nível de isolamento de uma transação em um objeto **Connection**. A configuração não tem efeito até a próxima vez que você chamar o método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se o nível de isolamento solicitado estiver indisponível, o provedor poderá retornar o maior nível seguinte de isolamento. Consulte a propriedade **IsolationLevel** na referência do programador do ADO para obter mais detalhes sobre os valores válidos.

## <a name="nested-transactions"></a>Transações aninhadas

Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.

