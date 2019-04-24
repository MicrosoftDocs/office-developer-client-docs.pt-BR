---
title: Propriedade CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295217"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="5e189-102">Propriedade CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="5e189-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="5e189-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e189-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e189-104">Indica o local do serviço de cursor.</span><span class="sxs-lookup"><span data-stu-id="5e189-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5e189-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5e189-105">Settings And Return Values</span></span>

<span data-ttu-id="5e189-106">Define ou retorna um valor **Long** que pode ser definido como um dos valores [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="5e189-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e189-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e189-107">Remarks</span></span>

<span data-ttu-id="5e189-p101">Essa propriedade permite que você escolha entre diversas bibliotecas de cursores acessíveis ao provedor. Geralmente, é possível escolher entre usar uma biblioteca de cursores do lado do cliente ou uma que esteja localizada no servidor.</span><span class="sxs-lookup"><span data-stu-id="5e189-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="5e189-p102">A definição dessa propriedade afeta as conexões estabelecidas apenas depois que a propriedade tiver sido configurada. A alteração da propriedade **CursorLocation** não afeta as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="5e189-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="5e189-p103">Os cursores retornados pelo método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) herdam essa definição. Os objetos **Recordset** herdarão automaticamente essa definição de suas conexões associadas.</span><span class="sxs-lookup"><span data-stu-id="5e189-p103">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="5e189-114">Essa propriedade é leitura/gravação em um [Connection](connection-object-ado.md) ou um [Recordset](recordset-object-ado.md) fechado e somente leitura em um **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="5e189-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="5e189-115">**Uso do Remote Data Service** Quando usado em um objeto **Recordset** ou **Connection** do lado do cliente, a propriedade **CursorLocation** só pode ser definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="5e189-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

