---
title: Propriedade Item (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462239"
---
# <a name="item-property-ado"></a><span data-ttu-id="b8515-102">Propriedade Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8515-102">Item Property (ADO)</span></span>

<span data-ttu-id="b8515-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8515-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b8515-104">Indica um membro específico de uma coleção, por nome ou número ordinal.</span><span class="sxs-lookup"><span data-stu-id="b8515-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8515-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8515-105">Syntax</span></span>

<span data-ttu-id="b8515-106">Definir o*objeto* = *conjunto*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="b8515-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="b8515-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8515-107">Return Value</span></span>

<span data-ttu-id="b8515-108">Retorna uma referência de objeto.</span><span class="sxs-lookup"><span data-stu-id="b8515-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8515-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8515-109">Parameters</span></span>

- <span data-ttu-id="b8515-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="b8515-110">*Index*</span></span>

- <span data-ttu-id="b8515-111">Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="b8515-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8515-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8515-112">Remarks</span></span>

<span data-ttu-id="b8515-113">Use a propriedade **Item** para retornar um objeto específico em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="b8515-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="b8515-114">Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="b8515-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="b8515-115">Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.</span><span class="sxs-lookup"><span data-stu-id="b8515-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="b8515-116">A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:</span><span class="sxs-lookup"><span data-stu-id="b8515-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
