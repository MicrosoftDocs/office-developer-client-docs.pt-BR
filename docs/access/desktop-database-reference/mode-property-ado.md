---
title: Propriedade Mode (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f30dac303541b0f53d06eb7756739ff1add6ce0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288866"
---
# <a name="mode-property-ado"></a><span data-ttu-id="01226-102">Propriedade Mode (ADO)</span><span class="sxs-lookup"><span data-stu-id="01226-102">Mode property (ADO)</span></span>


<span data-ttu-id="01226-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01226-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01226-104">Indica as permissões disponíveis para modificar os dados em um objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md) ou [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="01226-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="01226-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="01226-105">Settings and return values</span></span>

<span data-ttu-id="01226-p101">Define ou retorna um valor [ConnectModeEnum](connectmodeenum.md). O valor padrão para um objeto **Connection** é **adModeUnknown**. O valor padrão para um objeto **Record** é **adModeRead**. O valor padrão para um **Stream** associado a uma fonte de base (aberta com uma URL como a fonte ou como o padrão **Stream** de um **Record**) é **adModeRead**. O valor padrão para um objeto **Stream** não associado a uma fonte de base (instanciada na memória) é **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="01226-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="01226-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="01226-111">Remarks</span></span>

<span data-ttu-id="01226-p102">Use a propriedade **Mode** para definir ou retornar as permissões de acesso em uso pelo provedor na conexão atual. Você pode definir a propriedade **Mode** apenas quando o objeto **Connection** estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="01226-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="01226-p103">Para um objeto **Stream**, se o modo de acesso não for especificado, ele será herdado da fonte usada para abrir o objeto **Stream**. Por exemplo, se um **Stream** for aberto a partir de um objeto **Record**, por padrão, ele será aberto no mesmo modo que o **Record**.</span><span class="sxs-lookup"><span data-stu-id="01226-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="01226-116">Esta propriedade será leitura/gravação enquanto o objeto estiver fechado e somente leitura quando estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="01226-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="01226-117">**Uso do Remote Data Service** Quando usado em um objeto Connection do lado do cliente, a propriedade **Mode** só pode ser definida como **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="01226-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

