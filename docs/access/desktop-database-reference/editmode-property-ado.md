---
title: Propriedade EditMode (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462671"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="2d64b-102">Propriedade EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d64b-102">EditMode Property (ADO)</span></span>


<span data-ttu-id="2d64b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d64b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d64b-104">Indica o status de edição do registro atual.</span><span class="sxs-lookup"><span data-stu-id="2d64b-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d64b-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2d64b-105">Return Value</span></span>

<span data-ttu-id="2d64b-106">Retorna um valor [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="2d64b-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d64b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d64b-107">Remarks</span></span>

<span data-ttu-id="2d64b-p101">O ADO mantém um buffer de edição associado ao registro atual. Essa propriedade indica se as alterações foram feitas nesse buffer ou se um novo registro foi criado. Use a propriedade **EditMode** para determinar o status de edição do registro atual. É possível procurar alterações pendentes se um processo de edição tiver sido interrompido e determinar se você precisa usar o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2d64b-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="2d64b-112">Consulte o método [AddNew](addnew-method-ado.md) para obter uma descrição mais detalhada da propriedade **EditMode** em diferentes condições de edição.</span><span class="sxs-lookup"><span data-stu-id="2d64b-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="2d64b-113">Quando uma chamada para [Excluir](delete-method-ado-recordset.md) não exclui o registro com êxito ou registros nos dados de origem (devido a violações de integridade referencial, por exemplo), o [Recordset](recordset-object-ado.md) permanecerá no modo de edição (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="2d64b-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="2d64b-114">Isso significa que **CancelUpdate** deve ser chamado antes de sair do registro atual (com [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), por exemplo).</span><span class="sxs-lookup"><span data-stu-id="2d64b-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <P><span data-ttu-id="2d64b-p103">[!OBSERVAçãO] <STRONG>EditMode</STRONG> pode retornar um valor válido apenas se existir um registro atual. O <STRONG>EditMode</STRONG> retornará um erro se <A href="bof-eof-properties-ado.md">BOF ou EOF</A> for verdadeiro ou se o registro atual tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="2d64b-p103"><STRONG>EditMode</STRONG> can return a valid value only if there is a current record. <STRONG>EditMode</STRONG> will return an error if <A href="bof-eof-properties-ado.md">BOF or EOF</A> is true, or if the current record has been deleted.</span></span></P>


