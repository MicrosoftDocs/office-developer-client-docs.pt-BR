---
title: Propriedade Item (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290790"
---
# <a name="item-property-ado"></a><span data-ttu-id="c703c-102">Propriedade Item (ADO)</span><span class="sxs-lookup"><span data-stu-id="c703c-102">Item property (ADO)</span></span>

<span data-ttu-id="c703c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c703c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c703c-104">Indica um membro específico de uma coleção, por nome ou número ordinal.</span><span class="sxs-lookup"><span data-stu-id="c703c-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c703c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c703c-105">Syntax</span></span>

<span data-ttu-id="c703c-106">Definir *coleção de*  =  *objetos.* Item ( Index )</span><span class="sxs-lookup"><span data-stu-id="c703c-106">Set *object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="c703c-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c703c-107">Return value</span></span>

<span data-ttu-id="c703c-108">Retorna uma referência de objeto.</span><span class="sxs-lookup"><span data-stu-id="c703c-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="c703c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c703c-109">Parameters</span></span>

|<span data-ttu-id="c703c-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c703c-110">Parameter</span></span>|<span data-ttu-id="c703c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c703c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c703c-112">*Índice*</span><span class="sxs-lookup"><span data-stu-id="c703c-112">*Index*</span></span> |<span data-ttu-id="c703c-113">Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="c703c-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c703c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c703c-114">Remarks</span></span>

<span data-ttu-id="c703c-p101">Use a propriedade **Item** para retornar um objeto específico em uma coleção. Um erro ocorrerá se **Item** não puder encontrar um objeto na coleção correspondente ao argumento *Index*. Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.</span><span class="sxs-lookup"><span data-stu-id="c703c-p101">Use the **Item** property to return a specific object in a collection. If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs. Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="c703c-118">A propriedade **Item** é a propriedade padrão para todas as coleções; por esse motivo, os seguintes formulários de sintaxe são intercambiáveis:</span><span class="sxs-lookup"><span data-stu-id="c703c-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
