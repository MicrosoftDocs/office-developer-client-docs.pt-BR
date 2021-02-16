---
title: Função DateAdd (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Retorna uma data especificada com o intervalo de números especificado (inteiro positivo ou negativo) adicionado a uma parte de data especificada dessa data.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423199"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="36742-103">Função DateAdd (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="36742-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="36742-104">Retorna uma data especificada com o intervalo de números especificado (inteiro positivo ou negativo) adicionado a uma parte de data especificada dessa data.</span><span class="sxs-lookup"><span data-stu-id="36742-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="36742-105">O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="36742-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="36742-106">> Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="36742-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36742-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36742-107">Syntax</span></span>

<span data-ttu-id="36742-108">**DateAdd** (*DatePart*, *Número*, *Data*)</span><span class="sxs-lookup"><span data-stu-id="36742-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="36742-109">A **função DateAdd** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="36742-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="36742-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="36742-110">**Argument name**</span></span>|<span data-ttu-id="36742-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36742-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36742-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="36742-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="36742-113">A parte de  *Data à*  qual um número inteiro é adicionado.</span><span class="sxs-lookup"><span data-stu-id="36742-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="36742-114">Consulte a seção Comentários para ver a lista de configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="36742-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="36742-115">*Número*</span><span class="sxs-lookup"><span data-stu-id="36742-115">*Number*</span></span>  <br/> |<span data-ttu-id="36742-116">É uma expressão que pode ser resolvida para um inteiro que é adicionado a uma  *DatePart*  de  *Data*  .</span><span class="sxs-lookup"><span data-stu-id="36742-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="36742-117">Se você especificar um valor com uma fração decimal, a fração será truncada.</span><span class="sxs-lookup"><span data-stu-id="36742-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="36742-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="36742-118">*Date*</span></span>  <br/> |<span data-ttu-id="36742-119">Uma expressão que pode ser resolvida para um valor de Data/Hora.</span><span class="sxs-lookup"><span data-stu-id="36742-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="36742-120">A  *expressão do argumento Date,*  a expressão de coluna, a variável definida pelo usuário ou a cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="36742-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36742-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="36742-121">Remarks</span></span>

<span data-ttu-id="36742-122">A tabela a seguir lista todos os  *argumentos DatePart*  válidos.</span><span class="sxs-lookup"><span data-stu-id="36742-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="36742-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="36742-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="36742-124">**ano**</span><span class="sxs-lookup"><span data-stu-id="36742-124">**year**</span></span> <br/> |
|<span data-ttu-id="36742-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="36742-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="36742-126">**Mês**</span><span class="sxs-lookup"><span data-stu-id="36742-126">**month**</span></span> <br/> |
|<span data-ttu-id="36742-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="36742-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="36742-128">**dia**</span><span class="sxs-lookup"><span data-stu-id="36742-128">**day**</span></span> <br/> |
|<span data-ttu-id="36742-129">**semana**</span><span class="sxs-lookup"><span data-stu-id="36742-129">**week**</span></span> <br/> |
|<span data-ttu-id="36742-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="36742-130">**hour**</span></span> <br/> |
|<span data-ttu-id="36742-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="36742-131">**minute**</span></span> <br/> |
|<span data-ttu-id="36742-132">**segundo**</span><span class="sxs-lookup"><span data-stu-id="36742-132">**second**</span></span> <br/> |
|<span data-ttu-id="36742-133">**milissegundos**</span><span class="sxs-lookup"><span data-stu-id="36742-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="36742-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="36742-134">Example</span></span>

<span data-ttu-id="36742-135">A expressão a seguir calcula o último dia do mês atual.</span><span class="sxs-lookup"><span data-stu-id="36742-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="36742-136">A expressão a seguir calcula o último dia do mês anterior.</span><span class="sxs-lookup"><span data-stu-id="36742-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


