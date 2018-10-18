---
title: Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3de31156f9c06d3a14e7dbef2748543a3e6c4fd
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605755"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="dab3a-102">Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="dab3a-102">BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)</span></span>


<span data-ttu-id="dab3a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dab3a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="dab3a-104">Estes métodos de transação gerenciam o processamento das transações em um objeto [Connection](connection-object-ado.md) da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="dab3a-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

  - <span data-ttu-id="dab3a-105">**BeginTrans**  inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="dab3a-105">**BeginTrans** — Begins a new transaction.</span></span>

  - <span data-ttu-id="dab3a-p101">**CommitTrans**  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

  - <span data-ttu-id="dab3a-p102">**RollbackTrans**  cancela qualquer alteração feita durante a transação atual e finaliza a transação. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab3a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dab3a-110">Syntax</span></span>

<span data-ttu-id="dab3a-111">*nível* = *objeto*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="dab3a-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="dab3a-112">*objeto*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="dab3a-112">*object*.BeginTrans</span></span>

<span data-ttu-id="dab3a-113">*objeto*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="dab3a-113">*object*.CommitTrans</span></span>

<span data-ttu-id="dab3a-114">*objeto*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="dab3a-114">*object*.RollbackTrans</span></span>

<span data-ttu-id="dab3a-115"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="dab3a-115"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="dab3a-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dab3a-116">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="dab3a-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dab3a-117">Return value</span></span>
>>>>>>> <span data-ttu-id="dab3a-118">mestre</span><span class="sxs-lookup"><span data-stu-id="dab3a-118">master</span></span>

<span data-ttu-id="dab3a-119">**BeginTrans** pode ser chamado como uma função que retorna uma variável **Long**, que indica o nível de aninhamento da transação.</span><span class="sxs-lookup"><span data-stu-id="dab3a-119">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="dab3a-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab3a-120">Parameters</span></span>

  - <span data-ttu-id="dab3a-121">*object*</span><span class="sxs-lookup"><span data-stu-id="dab3a-121">*object*</span></span>

  - <span data-ttu-id="dab3a-122">Um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="dab3a-122">A **Connection** object.</span></span>

<span data-ttu-id="dab3a-123">**Objeto Connection**</span><span class="sxs-lookup"><span data-stu-id="dab3a-123">**Connection**</span></span>

<span data-ttu-id="dab3a-p103">Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dab3a-p104">Nem todos os provedores oferecem suporte a transações. Verifique se a propriedade "<STRONG>Transaction DDL</STRONG>" definida pelo provedor aparece na coleção <A href="properties-collection-ado.md">Properties</A> do objeto <STRONG>Connection</STRONG>, indicando o suporte do provedor a transações. Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p104">Not all providers support transactions. Verify that the provider-defined property "<STRONG>Transaction DDL</STRONG>" appears in the <STRONG>Connection</STRONG> object's <A href="properties-collection-ado.md">Properties</A> collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span></P>



<span data-ttu-id="dab3a-131">Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.</span><span class="sxs-lookup"><span data-stu-id="dab3a-131">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="dab3a-p105">Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="dab3a-p106">A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="dab3a-p107">Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.</span><span class="sxs-lookup"><span data-stu-id="dab3a-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

<span data-ttu-id="dab3a-141">**Remote Data Service**</span><span class="sxs-lookup"><span data-stu-id="dab3a-141">**Remote Data Service**</span></span>

<span data-ttu-id="dab3a-142">Os métodos **BeginTrans**, **CommitTrans** e **RollbackTrans** não estão disponíveis em um objeto **Connection** do cliente.</span><span class="sxs-lookup"><span data-stu-id="dab3a-142">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

