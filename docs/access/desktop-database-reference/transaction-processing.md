---
title: Processamento de transação
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a598b2842638b0c58e72ef2b802c8214f5c72b8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463201"
---
# <a name="transaction-processing"></a><span data-ttu-id="dcc0e-102">Processamento de transação</span><span class="sxs-lookup"><span data-stu-id="dcc0e-102">Transaction Processing</span></span>


<span data-ttu-id="dcc0e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcc0e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dcc0e-p101">O ADO fornece os seguintes métodos para controlar transações: **BeginTrans**, **CommitTrans** e **RollbackTrans**. Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p101">ADO provides the following methods for controlling transactions: **BeginTrans**, **CommitTrans**, and **RollbackTrans**. Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dcc0e-p102">Nem todos os provedores oferecem suporte a transações. Verifique se a propriedade "<STRONG>Transaction DDL</STRONG>" definida pelo provedor aparece na coleção <A href="properties-collection-ado.md">Properties</A> do objeto <STRONG>Connection</STRONG>, indicando o suporte do provedor a transações. Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p102">Not all providers support transactions. Verify that the provider-defined property "<STRONG>Transaction DDL</STRONG>" appears in the <STRONG>Connection</STRONG> object's <A href="properties-collection-ado.md">Properties</A> collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span></P>



<span data-ttu-id="dcc0e-112">Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-112">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="dcc0e-p103">A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p103">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="dcc0e-p104">Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p104">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** method may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

## <a name="transaction-isolation-level"></a><span data-ttu-id="dcc0e-119">Nível de isolamento de transação</span><span class="sxs-lookup"><span data-stu-id="dcc0e-119">Transaction Isolation Level</span></span>

<span data-ttu-id="dcc0e-p105">Use a propriedade **IsolationLevel** para definir o nível de isolamento de uma transação em um objeto **Connection**. A configuração não tem efeito até a próxima vez que você chamar o método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Se o nível de isolamento solicitado estiver indisponível, o provedor pode retornar o próximo nível de isolamento maior. Consulte a propriedade **IsolationLevel** na Referência do programador do ADO para obter mais detalhes sobre valores válidos.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p105">Use the **IsolationLevel** property to set the isolation level of a transaction on a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation. Refer to the **IsolationLevel** property in the ADO Programmer's Reference for more details on valid values.</span></span>

## <a name="nested-transactions"></a><span data-ttu-id="dcc0e-124">Transações aninhadas</span><span class="sxs-lookup"><span data-stu-id="dcc0e-124">Nested Transactions</span></span>

<span data-ttu-id="dcc0e-p106">Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="dcc0e-p106">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

