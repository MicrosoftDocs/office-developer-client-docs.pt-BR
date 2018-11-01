---
title: Propriedade DrilledDown (ADO MD)
TOCTitle: DrilledDown Property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7e53eb2a6d1735e07fa73e38adad8a59522fddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871497"
---
# <a name="drilleddown-property-ado-md"></a><span data-ttu-id="64d0c-102">Propriedade DrilledDown (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="64d0c-102">DrilledDown Property (ADO MD)</span></span>


<span data-ttu-id="64d0c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="64d0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64d0c-104">Indica se nenhum filho segue imediatamente o membro no eixo.</span><span class="sxs-lookup"><span data-stu-id="64d0c-104">Indicates whether no children immediately follow the member on the axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="64d0c-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="64d0c-105">Return values</span></span>

<span data-ttu-id="64d0c-p101">Retorna um valor **Boolean** e é somente leitura. **DrilledDown** retornará **True** se não houver membros filho do membro atual no eixo. **DrilledDown** retornará **False** se houver um ou mais membros filho do membro atual no eixo.</span><span class="sxs-lookup"><span data-stu-id="64d0c-p101">Returns a **Boolean** value and is read-only. **DrilledDown** returns **True** if there are no child members of the current member on the axis. **DrilledDown** returns **False** if there is one or more child members of the current member on the axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d0c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="64d0c-109">Remarks</span></span>

<span data-ttu-id="64d0c-p102">Use a propriedade **DrilledDown** para determinar se há pelo menos um filho desse membro no eixo imediatamente após esse membro. Essas informações são úteis na exibição do membro.</span><span class="sxs-lookup"><span data-stu-id="64d0c-p102">Use the **DrilledDown** property to determine whether there is at least one child of this member on the axis immediately following this member. This information is useful when displaying the member.</span></span>

<span data-ttu-id="64d0c-p103">Somente objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Position](position-object-ado-md.md) oferecem suporte a essa propriedade. Ocorrerá um erro quando ela for referenciada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="64d0c-p103">This property is only supported on [Member](member-object-ado-md.md) objects belonging to a [Position](position-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span>

