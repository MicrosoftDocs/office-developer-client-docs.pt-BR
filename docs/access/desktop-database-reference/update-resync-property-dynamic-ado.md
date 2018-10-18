---
title: Propriedade Update Resync -- Dinâmica (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604418"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="34d64-102">Propriedade Update Resync -- Dinâmica (ADO)</span><span class="sxs-lookup"><span data-stu-id="34d64-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="34d64-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34d64-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34d64-104">Especifica se o método [UpdateBatch](updatebatch-method-ado.md) é seguido por uma operação de método [Resync](resync-method-ado.md) implícita e, em caso positivo, o escopo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="34d64-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

<span data-ttu-id="34d64-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="34d64-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="34d64-106">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="34d64-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="34d64-107">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="34d64-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="34d64-108">mestre</span><span class="sxs-lookup"><span data-stu-id="34d64-108">master</span></span>

<span data-ttu-id="34d64-109">Define ou retorna uma ou mais do [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.</span><span class="sxs-lookup"><span data-stu-id="34d64-109">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d64-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="34d64-110">Remarks</span></span>

<span data-ttu-id="34d64-111">Os valores de ADCPROP\_UPDATERESYNC\_ENUM pode ser combinado, exceto para adresyncall, que já representa a combinação do restante dos valores.</span><span class="sxs-lookup"><span data-stu-id="34d64-111">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="34d64-112">A constante **adResyncConflicts** armazena os valores de ressincronização como valores de base, mas não substitui as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="34d64-112">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="34d64-113">**Update Resync** é uma propriedade dinâmica acrescentada à coleção [Properties](recordset-object-ado.md) do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for configurada como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="34d64-113">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

