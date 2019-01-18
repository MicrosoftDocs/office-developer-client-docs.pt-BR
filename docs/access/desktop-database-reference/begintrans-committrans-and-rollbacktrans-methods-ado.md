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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720328"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="3f9ee-102">Métodos BeginTrans, CommitTrans e RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="3f9ee-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="3f9ee-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f9ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f9ee-104">Estes métodos de transação gerenciam o processamento das transações em um objeto [Connection](connection-object-ado.md) da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3f9ee-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="3f9ee-105">**BeginTrans**  inicia uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="3f9ee-p101">**CommitTrans**  salva as alterações e finaliza a transação atual. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

- <span data-ttu-id="3f9ee-p102">**RollbackTrans**  cancela qualquer alteração feita durante a transação atual e finaliza a transação. Também pode iniciar uma nova transação.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9ee-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f9ee-110">Syntax</span></span>

<span data-ttu-id="3f9ee-111">*nível* = *objeto*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="3f9ee-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="3f9ee-112">*objeto*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="3f9ee-112">*object*.BeginTrans</span></span>

<span data-ttu-id="3f9ee-113">*objeto*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="3f9ee-113">*object*.CommitTrans</span></span>

<span data-ttu-id="3f9ee-114">*objeto*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="3f9ee-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="3f9ee-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3f9ee-115">Return value</span></span>

<span data-ttu-id="3f9ee-116">**BeginTrans** pode ser chamado como uma função que retorna uma variável **Long**, que indica o nível de aninhamento da transação.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f9ee-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f9ee-117">Parameters</span></span>

|<span data-ttu-id="3f9ee-118">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f9ee-118">Parameter</span></span>|<span data-ttu-id="3f9ee-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f9ee-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3f9ee-120">*objeto*</span><span class="sxs-lookup"><span data-stu-id="3f9ee-120">*object*</span></span> |<span data-ttu-id="3f9ee-121">Um objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-121">A **Connection** object.</span></span>|

### <a name="connection"></a><span data-ttu-id="3f9ee-122">Connection</span><span class="sxs-lookup"><span data-stu-id="3f9ee-122">Connection</span></span>

<span data-ttu-id="3f9ee-p103">Use esses métodos com um objeto **Connection** quando desejar salvar ou cancelar uma série de alterações feitas na fonte de dados como uma única unidade. Por exemplo, para transferir dinheiro entre contas, subtraia um valor de uma conta e acrescente o mesmo valor à outra. Se uma das duas atualizações falhar, as contas ficarão desequilibradas. A realização dessas alterações em uma transação aberta garante que todas as alterações, ou nenhuma delas, ocorram.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="3f9ee-127">[!OBSERVAçãO] Nem todos os provedores oferecem suporte a transações.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-127">Not all providers support transactions.</span></span> <span data-ttu-id="3f9ee-128">Verifique se a propriedade definido pelo provedor **Transação DDL** aparece no conjunto de [Propriedades](properties-collection-ado.md) do objeto de **Conexão** , indicando que o provedor oferece suporte às transações.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-128">Verify that the provider-defined property **Transaction DDL** appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="3f9ee-129">Se o provedor não oferecer esse suporte, um erro ocorrerá quando você chamar um desses métodos.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-129">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="3f9ee-130">Depois que você chamar o método **BeginTrans**, o provedor não confirmará mais instantaneamente as alterações feitas até que **CommitTrans** ou **RollbackTrans** seja chamado para finalizar a transação.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-130">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="3f9ee-p105">Para os provedores que oferecem suporte a transações aninhadas, uma nova transação aninhada será iniciada quando você chamar o método **BeginTrans** em uma transação aberta. O valor de retorno indica o nível de aninhamento: o valor de retorno "1" indica que você abriu uma transação de nível superior (ou seja, a transação não está aninhada em outra transação), "2" indica que você abriu uma transação de segundo nível e assim por diante. A chamada de **CommitTrans** ou **RollbackTrans** afeta apenas a transação aberta mais recentemente; você deve fechar ou reverter a transação atual antes de resolver qualquer transação de nível superior.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="3f9ee-p106">A chamada do método **CommitTrans** salva as alterações feitas em uma transação aberta na conexão e finaliza a transação. A chamada do método **RollbackTrans** reverte qualquer alteração feita em uma transação aberta e finaliza a transação. A chamada de um desses dois métodos quando não houver transação aberta gerará erro.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="3f9ee-p107">Dependendo da propriedade **Attributes** do objeto [Connection](attributes-property-ado.md), a chamada do método **CommitTrans** ou **RollbackTrans** poderá iniciar automaticamente uma nova transação. Se a propriedade **Attributes** for definida como **adXactCommitRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **CommitTrans**. Se a propriedade **Attributes** for definida como **adXactAbortRetaining**, o provedor iniciará automaticamente uma nova transação após a chamada de **RollbackTrans**.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="3f9ee-140">Remote Data Service</span><span class="sxs-lookup"><span data-stu-id="3f9ee-140">Remote Data Service</span></span>

<span data-ttu-id="3f9ee-141">Os métodos **BeginTrans**, **CommitTrans** e **RollbackTrans** não estão disponíveis em um objeto **Connection** do cliente.</span><span class="sxs-lookup"><span data-stu-id="3f9ee-141">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

