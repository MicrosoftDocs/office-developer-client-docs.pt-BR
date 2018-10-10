---
title: Propriedade Description (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29c6723d710fcf3a8114fb4460326d87261c3fc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462667"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="d836f-102">Propriedade Description (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d836f-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="d836f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d836f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d836f-104">Retorna uma explicação do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="d836f-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="d836f-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d836f-105">Return Values</span></span>

<span data-ttu-id="d836f-106">Retorna um objeto **String** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d836f-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d836f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d836f-107">Remarks</span></span>

<span data-ttu-id="d836f-p101">No caso de objetos [Member](member-object-ado-md.md), **Description** aplica-se somente a membros de medida e de fórmula. **Description** retorna uma sequência de caracteres vazia ("") para todos os outros tipos de membros. Para obter mais informações sobre os vários tipos de membros, consulte a propriedade [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d836f-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="d836f-p102">Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a essa propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d836f-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

