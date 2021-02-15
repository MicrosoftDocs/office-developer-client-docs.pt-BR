---
title: Propriedade Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293935"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="24b02-102">Propriedade Description (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="24b02-102">Description property (ADO MD)</span></span>


<span data-ttu-id="24b02-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24b02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24b02-104">Retorna uma explicação do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="24b02-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="24b02-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24b02-105">Return values</span></span>

<span data-ttu-id="24b02-106">Retorna **String** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="24b02-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b02-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="24b02-107">Remarks</span></span>

<span data-ttu-id="24b02-p101">No caso de objetos [Member](member-object-ado-md.md), **Description** aplica-se somente a membros de medida e de fórmula. **Description** retorna uma sequência de caracteres vazia ("") para todos os outros tipos de membros. Para obter mais informações sobre os vários tipos de membros, consulte a propriedade [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="24b02-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="24b02-p102">Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a essa propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="24b02-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

