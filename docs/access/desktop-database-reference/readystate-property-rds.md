---
title: Propriedade ReadyState (RDS)
TOCTitle: ReadyState Property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a22099e49489226c7848a54112e7ab5e70b64ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603914"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="e18f9-102">Propriedade ReadyState (RDS)</span><span class="sxs-lookup"><span data-stu-id="e18f9-102">ReadyState Property (RDS)</span></span>


<span data-ttu-id="e18f9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e18f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e18f9-104">Indica o progresso de um objeto [DataControl](datacontrol-object-rds.md) à medida que ele recupera dados em seu objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e18f9-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="e18f9-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="e18f9-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e18f9-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e18f9-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e18f9-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e18f9-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e18f9-108">mestre</span><span class="sxs-lookup"><span data-stu-id="e18f9-108">master</span></span>

<span data-ttu-id="e18f9-109">Define ou retorna um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="e18f9-109">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e18f9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e18f9-110">Value</span></span></p></th>
<th><p><span data-ttu-id="e18f9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e18f9-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e18f9-112"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="e18f9-112"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="e18f9-p101">A consulta atual ainda está sendo executada e nenhuma linha foi pesquisada. O <strong>Recordset</strong> do objeto <strong>DataControl</strong> não está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="e18f9-p101">The current query is still executing and no rows have been fetched. The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e18f9-115"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="e18f9-115"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="e18f9-p102">Um conjunto inicial de linhas recuperado pela consulta atual foi armazenado no <strong>Recordset</strong> do objeto <strong>DataControl</strong> e está disponível para uso. As linhas restantes ainda estão sendo pesquisadas.</span><span class="sxs-lookup"><span data-stu-id="e18f9-p102">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use. The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e18f9-118"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="e18f9-118"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="e18f9-119">Todas as linhas recuperadas pela consulta atual foram armazenadas no <strong>Recordset</strong> do objeto <strong>DataControl</strong> e estão disponíveis para uso.
</span><span class="sxs-lookup"><span data-stu-id="e18f9-119">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="e18f9-120">Este estado também é possível se uma operação for anulada devido a um erro ou se o objeto <strong>Recordset</strong> não for inicializado.</span><span class="sxs-lookup"><span data-stu-id="e18f9-120">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="e18f9-p104">[!OBSERVAçãO] Cada arquivo executável do lado do cliente que utilizar essas constantes deverá fornecer suas respectivas declarações. Você pode recortar e colar as declarações da constante que deseja do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="e18f9-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="e18f9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e18f9-123">Remarks</span></span>

<span data-ttu-id="e18f9-p105">Utilize o evento [onReadyStateChange](onreadystatechange-event-rds.md) para monitorar as alterações da propriedade **ReadyState** durante uma operação de consulta assíncrona. Esse procedimento é mais eficiente do que verificar periodicamente o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e18f9-p105">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation. This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="e18f9-126">Se ocorrer um erro durante uma operação assíncrona, a propriedade **ReadyState** será alterada para **adcReadyStateComplete**, a propriedade [State](state-property-ado.md) será alterada de **adStateExecuting** para **adStateClosed**e o **conjunto de registros** propriedade [Value](value-property-ado.md) do objeto permanecerá como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="e18f9-126">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

