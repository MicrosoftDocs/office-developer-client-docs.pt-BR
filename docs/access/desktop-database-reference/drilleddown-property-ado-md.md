---
title: Propriedade DrilledDown (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40a97c7f755f681169c77c3a2077ee41d9cdc980
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712446"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="81c94-102">Propriedade DrilledDown (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="81c94-102">DrilledDown property (ADO MD)</span></span>


<span data-ttu-id="81c94-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="81c94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81c94-104">Indica se nenhum filho segue imediatamente o membro no eixo.</span><span class="sxs-lookup"><span data-stu-id="81c94-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="81c94-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="81c94-105">Return values</span></span>

<span data-ttu-id="81c94-p101">Retorna um valor **Boolean** e é somente leitura. **DrilledDown** retornará **True** se não houver membros filho do membro atual no eixo. **DrilledDown** retornará **False** se houver um ou mais membros filho do membro atual no eixo.</span><span class="sxs-lookup"><span data-stu-id="81c94-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="81c94-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="81c94-109">Remarks</span></span>

<span data-ttu-id="81c94-p102">Use a propriedade **DrilledDown** para determinar se há pelo menos um filho desse membro no eixo imediatamente após esse membro. Essas informações são úteis na exibição do membro.</span><span class="sxs-lookup"><span data-stu-id="81c94-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="81c94-p103">Somente objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Position](position-object-ado-md.md) oferecem suporte a essa propriedade. Ocorrerá um erro quando ela for referenciada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="81c94-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

