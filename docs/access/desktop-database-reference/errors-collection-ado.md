---
title: Coleção Errors (ADO)
TOCTitle: Errors Collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 568524bf2be93720ec319b48a784dfc62bd03f65
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863301"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="e7484-102">Coleção Errors (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7484-102">Errors Collection (ADO)</span></span>


<span data-ttu-id="e7484-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7484-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e7484-104">Contém todos os objetos [Error](error-object-ado.md) criados em resposta à falha relacionada a um único provedor.</span><span class="sxs-lookup"><span data-stu-id="e7484-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7484-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7484-105">Remarks</span></span>

<span data-ttu-id="e7484-p101">Qualquer operação envolvendo os objetos ADO pode gerar um ou vários erros de provedor. À medida que cada erro ocorrer, um ou vários objetos **Error** poderão ser colocados na coleção **Errors** do objeto [Connection](connection-object-ado.md). Quando outra operação do ADO gerar um erro, a coleção **Errors** será limpa e o novo conjunto de objetos **Error** poderá ser colocado na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e7484-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object. When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="e7484-p102">Cada objeto **Error** representa um erro de provedor específico e não um erro do ADO. Os erros do ADO são apresentados no mecanismo de tratamento de exceções do tempo de execução. Por exemplo, no Microsoft Visual Basic, a ocorrência de um erro específico do ADO disparará um evento [onError](onerror-event-rds.md) e aparecerá no objeto **Err**.</span><span class="sxs-lookup"><span data-stu-id="e7484-p102">Each **Error** object represents a specific provider error, not an ADO error. ADO errors are exposed to the run-time exception-handling mechanism. For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="e7484-p103">As operações do ADO que não geram um erro não têm efeito sobre a coleção **Errors**. Use o método [Clear](clear-method-ado.md) para limpar manualmente a coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e7484-p103">ADO operations that don't generate an error have no effect on the **Errors** collection. Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="e7484-p104">O conjunto de objetos **Error** na coleção **Errors** descreve todos os erros que ocorreram em resposta a uma única instrução. A enumeração dos erros específicos na coleção **Errors** permite rotinas de tratamento de erros para determinar de modo mais preciso a causa e a origem de um erro e executar as etapas apropriadas para recuperação.</span><span class="sxs-lookup"><span data-stu-id="e7484-p104">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement. Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="e7484-p105">Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md), o método [Open](open-method-ado-connection.md) em um objeto **Connection** ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, você pode ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para verificar os avisos retornados.</span><span class="sxs-lookup"><span data-stu-id="e7484-p105">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="e7484-119">[!OBSERVAçãO] Consulte o tópico do objeto **Error** para obter uma explicação mais detalhada sobre como uma operação do ADO simples pode gerar erros múltiplos.</span><span class="sxs-lookup"><span data-stu-id="e7484-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


