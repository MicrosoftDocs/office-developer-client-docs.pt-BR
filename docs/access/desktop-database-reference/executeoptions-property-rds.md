---
title: Propriedade Executeoptions (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293249"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="b6939-102">Propriedade Executeoptions (RDS)</span><span class="sxs-lookup"><span data-stu-id="b6939-102">ExecuteOptions property (RDS)</span></span>


<span data-ttu-id="b6939-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6939-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6939-104">Indica se a execução assíncrona está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b6939-104">Indicates whether asynchronous execution is enabled.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b6939-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b6939-105">Settings and return values</span></span>

<span data-ttu-id="b6939-106">Define ou retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6939-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6939-107">Constante</span><span class="sxs-lookup"><span data-stu-id="b6939-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="b6939-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6939-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6939-109"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="b6939-109"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="b6939-110">Executa a próxima atualização do <a href="recordset-object-ado.md">Recordset</a> de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="b6939-110">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6939-111"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="b6939-111"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="b6939-112">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b6939-112">Default.</span></span> <span data-ttu-id="b6939-113">Executa a próxima atualização do <strong>Recordset</strong> de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b6939-113">Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b6939-p102">[!OBSERVAçãO] Cada arquivo executável do lado do cliente que usa essas constantes deve fornecer declarações para elas. Você pode recortar e colar as declarações de constantes desejadas do arquivo Adcvbs.inc, localizado na pasta C:\Arquivos de Programas\Arquivos Comuns\System\MSADC.</span><span class="sxs-lookup"><span data-stu-id="b6939-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6939-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6939-116">Remarks</span></span>

<span data-ttu-id="b6939-117">Se **ExecuteOptions** for definido como **adcExecAsync**, a próxima chamada do **Refresh** no **Recordset** do objeto [RDS.DataControl](datacontrol-object-rds.md) será executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b6939-117">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="b6939-118">Ocorrerá um erro se você tentar chamar [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) ou [Recordset](recordset-sourcerecordset-properties-rds.md) enquanto outra operação assíncrona que possa alterar o **Recordset** do objeto [RDS.DataControl](datacontrol-object-rds.md) estiver sendo executada.</span><span class="sxs-lookup"><span data-stu-id="b6939-118">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="b6939-119">Se ocorrer um erro durante uma operação assíncrona, o valor [ReadyState](readystate-property-rds.md) do objeto **RDS.DataControl** será alterado de **adcReadyStateLoaded** para **adcReadyStateComplete**, e o valor da propriedade **Recordset** permanecerá *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="b6939-119">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

