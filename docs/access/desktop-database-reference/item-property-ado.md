---
title: Propriedade Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949359"
---
# <a name="item-property-ado"></a><span data-ttu-id="c791c-102">Propriedade Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="c791c-102">Item property (ADO)</span></span>

<span data-ttu-id="c791c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c791c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c791c-104">Indica um membro específico de uma coleção, por nome ou número ordinal.</span><span class="sxs-lookup"><span data-stu-id="c791c-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c791c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c791c-105">Syntax</span></span>

<span data-ttu-id="c791c-106">Definir o*objeto* = *conjunto*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="c791c-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="c791c-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c791c-107">Return value</span></span>

<span data-ttu-id="c791c-108">Retorna uma referência de objeto.</span><span class="sxs-lookup"><span data-stu-id="c791c-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="c791c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c791c-109">Parameters</span></span>

|<span data-ttu-id="c791c-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c791c-110">Parameter</span></span>|<span data-ttu-id="c791c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c791c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c791c-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="c791c-112">*Index*</span></span> |<span data-ttu-id="c791c-113">Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c791c-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c791c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c791c-114">Remarks</span></span>

<span data-ttu-id="c791c-115">Use a propriedade **Item** para retornar um objeto específico em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c791c-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="c791c-116">Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="c791c-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="c791c-117">Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.</span><span class="sxs-lookup"><span data-stu-id="c791c-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="c791c-118">A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:</span><span class="sxs-lookup"><span data-stu-id="c791c-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
