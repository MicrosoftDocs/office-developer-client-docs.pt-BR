---
title: Método Open (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703829"
---
# <a name="open-method-ado-md"></a><span data-ttu-id="27094-102">Método Open (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="27094-102">Open method (ADO MD)</span></span>

<span data-ttu-id="27094-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="27094-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27094-104">Recupera os resultados de uma consulta multidimensional e retorna os resultados para um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="27094-104">Retrieves the results of a multidimensional query and returns the results to a cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="27094-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27094-105">Syntax</span></span>

<span data-ttu-id="27094-106">*Conjunto de células*. Abrir*fonte*, *ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="27094-106">*Cellset*.Open*Source*, *ActiveConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="27094-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27094-107">Parameters</span></span>

|<span data-ttu-id="27094-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="27094-108">Parameter</span></span>|<span data-ttu-id="27094-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="27094-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="27094-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="27094-110">*Source*</span></span> |<span data-ttu-id="27094-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27094-111">Optional.</span></span> <span data-ttu-id="27094-112">Um objeto **Variant** que resulta em uma consulta multidimensional válida, como uma consulta MDX (Expressão Multidimensional).</span><span class="sxs-lookup"><span data-stu-id="27094-112">A **Variant** that evaluates to a valid multidimensional query, such as a Multidimensional Expression (MDX) query.</span></span> <span data-ttu-id="27094-113">O argumento *Source* corresponde à propriedade [Source](source-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="27094-113">The *Source* argument corresponds to the [Source](source-property-ado-md.md) property.</span></span> <span data-ttu-id="27094-114">Para obter mais informações sobre MDX, consulte a documentação do OLE DB para OLAP no Microsoft Data Access Components SDK.</span><span class="sxs-lookup"><span data-stu-id="27094-114">For more information about MDX, see the OLE DB for OLAP documentation in the Microsoft Data Access Components SDK.</span></span>|
|<span data-ttu-id="27094-115">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="27094-115">*ActiveConnection*</span></span> |<span data-ttu-id="27094-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="27094-116">Optional.</span></span> <span data-ttu-id="27094-117">Um objeto **Variant** que resulta em uma sequência de caracteres que especifica um nome de variável de objeto [Connection](connection-object-ado.md) válido do ADO ou em uma definição de conexão.</span><span class="sxs-lookup"><span data-stu-id="27094-117">A **Variant** that evaluates to a string specifying either a valid ADO [Connection](connection-object-ado.md) object variable name or a definition for a connection.</span></span> <span data-ttu-id="27094-118">O argumento *ActiveConnection* Especifica a conexão para abrir o objeto de [conjunto de células](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="27094-118">The *ActiveConnection* argument specifies the connection in which to open the [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="27094-119">Se você passar uma definição de conexão para esse argumento, o ADO abrirá uma nova conexão utilizando os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="27094-119">If you pass a connection definition for this argument, ADO opens a new connection using the specified parameters.</span></span> <span data-ttu-id="27094-120">O argumento *ActiveConnection* corresponde à propriedade [ActiveConnection](activeconnection-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="27094-120">The *ActiveConnection* argument corresponds to the [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="27094-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="27094-121">Remarks</span></span>

<span data-ttu-id="27094-122">O método **Open** gerará um erro se um desses parâmetros for omitido e o valor de sua propriedade correspondente não tiver sido definido antes da tentativa de abrir o **Cellset**.</span><span class="sxs-lookup"><span data-stu-id="27094-122">The **Open** method generates an error if either of its parameters is omitted and its corresponding property value has not been set prior to attempting to open the **Cellset**.</span></span>

