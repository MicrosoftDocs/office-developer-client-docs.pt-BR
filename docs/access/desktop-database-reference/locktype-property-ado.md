---
title: Propriedade LockType (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289840"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="daf3f-102">Propriedade LockType (ADO)</span><span class="sxs-lookup"><span data-stu-id="daf3f-102">LockType property (ADO)</span></span>


<span data-ttu-id="daf3f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daf3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf3f-104">Indica o tipo de bloqueio colocado nos registros durante a edição.</span><span class="sxs-lookup"><span data-stu-id="daf3f-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="daf3f-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="daf3f-105">Settings and return values</span></span>

<span data-ttu-id="daf3f-106">Define ou retorna um valor [LockTypeEnum](locktypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="daf3f-106">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="daf3f-107">O valor padrão é **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="daf3f-107">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf3f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf3f-108">Remarks</span></span>

<span data-ttu-id="daf3f-p102">Defina a propriedade **LockType** antes de abrir um [Recordset](recordset-object-ado.md) para especificar qual tipo de bloqueio o provedor deve usar ao abri-lo. Leia a propriedade para retornar o tipo de bloqueio em uso em um objeto **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="daf3f-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="daf3f-p103">Talvez os provedores não ofereçam suporte a todos os tipos de bloqueio. Se um provedor não puder oferecer suporte à definição de **LockType** solicitada, ele substituirá outro tipo de bloqueio. Para determinar a funcionalidade real do bloqueio disponível em um objeto **Recordset**, use o método [Supports](supports-method-ado.md) com **adUpdate** e **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="daf3f-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="daf3f-p104">A definição **adLockPessimistic** não terá suporte se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, não ocorrerá nenhum erro; o **LockType** com suporte mais próximo será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="daf3f-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="daf3f-116">A propriedade **LockType** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="daf3f-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="daf3f-117">**Uso do Remote Data Service** Quando usado em um objeto Recordset do lado do cliente, \*\*\*\* a propriedade LockType só pode ser definida como **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="daf3f-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

