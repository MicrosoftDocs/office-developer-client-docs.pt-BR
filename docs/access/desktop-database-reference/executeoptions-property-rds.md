---
title: Propriedade ExecuteOptions (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6db51927182008314da045021f81e6547d5d78be
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026138"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="fbb3d-102">Propriedade ExecuteOptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="fbb3d-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="fbb3d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbb3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbb3d-104">Indica se a execução assíncrona está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fbb3d-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fbb3d-105">Settings and return values</span></span>

<span data-ttu-id="fbb3d-106">Define ou retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fbb3d-107">Constante</span><span class="sxs-lookup"><span data-stu-id="fbb3d-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="fbb3d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbb3d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbb3d-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="fbb3d-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="fbb3d-110">Executa a próxima atualização do <a href="recordset-object-ado.md">Recordset</a> de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbb3d-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="fbb3d-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="fbb3d-p101">Padrão. Executa a próxima atualização do <strong>Recordset</strong> de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fbb3d-p102">[!OBSERVAçãO] Cada arquivo executável do lado do cliente que usa essas constantes deve fornecer declarações para elas. Você pode recortar e colar as declarações de constantes desejadas do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb3d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbb3d-116">Remarks</span></span>

<span data-ttu-id="fbb3d-117">Se **ExecuteOptions** for definido como **adcExecAsync**, a próxima chamada do **Refresh** no [Recordset](datacontrol-object-rds.md) do objeto **RDS.DataControl** será executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="fbb3d-118">Ocorrerá um erro se você tentar chamar [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) enquanto outra operação assíncrona que possa alterar o [Recordset](datacontrol-object-rds.md) do objeto **RDS.DataControl** estiver sendo executada.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="fbb3d-119">Se ocorrer um erro durante uma operação assíncrona, o valor [ReadyState](readystate-property-rds.md) do objeto **RDS.DataControl** será alterado de **adcReadyStateLoaded** para **adcReadyStateComplete**, e o valor da propriedade **Recordset** permanecerá *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="fbb3d-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

