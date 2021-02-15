---
title: Propriedade dinâmica Update Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308341"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="11366-102">Propriedade dinâmica Update Resync (ADO)</span><span class="sxs-lookup"><span data-stu-id="11366-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="11366-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11366-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11366-104">Especifica se o método [UpdateBatch](updatebatch-method-ado.md) é seguido por uma operação de método [Resync](resync-method-ado.md) implícita e, em caso positivo, o escopo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="11366-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="11366-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="11366-105">Settings and return values</span></span>

<span data-ttu-id="11366-106">Define ou retorna um ou mais dos valores [ENUM ADCPROP \_ UPDATERESYNC. \_ ](adcprop-updateresync-enum.md)</span><span class="sxs-lookup"><span data-stu-id="11366-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="11366-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="11366-107">Remarks</span></span>

<span data-ttu-id="11366-108">Os valores de ENUM ADCPROP UPDATERESYNC podem ser combinados, exceto \_ adResyncAll, que já representa a combinação do restante \_ dos valores.</span><span class="sxs-lookup"><span data-stu-id="11366-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="11366-109">A constante **adResyncConflicts** armazena os valores de ressincronização como valores de base, mas não substitui as alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="11366-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="11366-110">**Update Resync** é uma propriedade dinâmica acrescentada à coleção [Properties](recordset-object-ado.md) do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for configurada como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="11366-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

