---
title: Propriedade CursorLocation (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463763"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="4259a-102">Propriedade CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="4259a-102">CursorLocation Property (ADO)</span></span>


<span data-ttu-id="4259a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4259a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4259a-104">Indica o local do serviço de cursor.</span><span class="sxs-lookup"><span data-stu-id="4259a-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4259a-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="4259a-105">Settings And Return Values</span></span>

<span data-ttu-id="4259a-106">Define ou retorna um valor **Long** que pode ser definido como um dos valores [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="4259a-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4259a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4259a-107">Remarks</span></span>

<span data-ttu-id="4259a-p101">Essa propriedade permite que você escolha entre diversas bibliotecas de cursores acessíveis ao provedor. Geralmente, é possível escolher entre usar uma biblioteca de cursores do lado do cliente ou uma que esteja localizada no servidor.</span><span class="sxs-lookup"><span data-stu-id="4259a-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="4259a-p102">A definição dessa propriedade afeta as conexões estabelecidas apenas depois que a propriedade tiver sido configurada. A alteração da propriedade **CursorLocation** não afeta as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="4259a-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="4259a-p103">Os cursores retornados pelo método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) herdam essa definição. Os objetos **Recordset** herdarão automaticamente essa definição de suas conexões associadas.</span><span class="sxs-lookup"><span data-stu-id="4259a-p103">Cursors returned by the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="4259a-114">Essa propriedade é leitura/gravação em um [Connection](connection-object-ado.md) ou um [Recordset](recordset-object-ado.md) fechado e somente leitura em um **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="4259a-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="4259a-115">**Uso de serviço de dados remotos** Quando usado em um cliente **Recordset** ou um objeto de **Conexão** , a propriedade **CursorLocation** só pode ser definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="4259a-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

