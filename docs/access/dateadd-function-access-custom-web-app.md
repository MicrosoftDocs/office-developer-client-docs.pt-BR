---
title: Função DateAdd (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Retorna uma data especificada com o intervalo de número especificado (inteiro positivo ou negativo) adicionada à parte dessa data data especificada.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765086"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="a025b-103">Função DateAdd (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a025b-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="a025b-104">Retorna uma data especificada com o intervalo de número especificado (inteiro positivo ou negativo) adicionada à parte dessa data data especificada.</span><span class="sxs-lookup"><span data-stu-id="a025b-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a025b-105">O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.*</span><span class="sxs-lookup"><span data-stu-id="a025b-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="a025b-106">> Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a025b-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a025b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a025b-107">Syntax</span></span>

<span data-ttu-id="a025b-108">**DateAdd** (*DatePart*, *número*, *Data*)</span><span class="sxs-lookup"><span data-stu-id="a025b-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="a025b-109">A função **DateAdd** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a025b-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a025b-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="a025b-110">**Argument name**</span></span>|<span data-ttu-id="a025b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a025b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a025b-112">*ParteDeData*</span><span class="sxs-lookup"><span data-stu-id="a025b-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="a025b-113">A parte da *Data* à qual um número inteiro é adicionado.</span><span class="sxs-lookup"><span data-stu-id="a025b-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="a025b-114">Consulte a seção de comentários para a lista das configurações válidas.</span><span class="sxs-lookup"><span data-stu-id="a025b-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="a025b-115">*Número*</span><span class="sxs-lookup"><span data-stu-id="a025b-115">*Number*</span></span>  <br/> |<span data-ttu-id="a025b-116">É uma expressão que possa ser resolvida para um número inteiro que é adicionado a um *DatePart* de *Data* .</span><span class="sxs-lookup"><span data-stu-id="a025b-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="a025b-117">Se você especificar um valor com uma fração decimal, a fração será truncada.</span><span class="sxs-lookup"><span data-stu-id="a025b-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="a025b-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="a025b-118">*Date*</span></span>  <br/> |<span data-ttu-id="a025b-119">Uma expressão que pode ser resolvida como um valor de data/hora.</span><span class="sxs-lookup"><span data-stu-id="a025b-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="a025b-120">A expressão de argumento *Data* , expressão de coluna, a variável definida pelo usuário ou cadeia de caracteres literal.</span><span class="sxs-lookup"><span data-stu-id="a025b-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a025b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a025b-121">Remarks</span></span>

<span data-ttu-id="a025b-122">A tabela a seguir lista todos os argumentos *DatePart* válidos.</span><span class="sxs-lookup"><span data-stu-id="a025b-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="a025b-123">***ParteDeData***</span><span class="sxs-lookup"><span data-stu-id="a025b-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="a025b-124">**year**</span><span class="sxs-lookup"><span data-stu-id="a025b-124">**year**</span></span> <br/> |
|<span data-ttu-id="a025b-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="a025b-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="a025b-126">**Mês**</span><span class="sxs-lookup"><span data-stu-id="a025b-126">**month**</span></span> <br/> |
|<span data-ttu-id="a025b-127">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="a025b-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="a025b-128">**day**</span><span class="sxs-lookup"><span data-stu-id="a025b-128">**day**</span></span> <br/> |
|<span data-ttu-id="a025b-129">**semana**</span><span class="sxs-lookup"><span data-stu-id="a025b-129">**week**</span></span> <br/> |
|<span data-ttu-id="a025b-130">**hora**</span><span class="sxs-lookup"><span data-stu-id="a025b-130">**hour**</span></span> <br/> |
|<span data-ttu-id="a025b-131">**minuto**</span><span class="sxs-lookup"><span data-stu-id="a025b-131">**minute**</span></span> <br/> |
|<span data-ttu-id="a025b-132">**segundo**</span><span class="sxs-lookup"><span data-stu-id="a025b-132">**second**</span></span> <br/> |
|<span data-ttu-id="a025b-133">**milissegundo**</span><span class="sxs-lookup"><span data-stu-id="a025b-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="a025b-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a025b-134">Example</span></span>

<span data-ttu-id="a025b-135">A expressão a seguir calcula o último dia do mês atual.</span><span class="sxs-lookup"><span data-stu-id="a025b-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="a025b-136">A expressão a seguir calcula o último dia do mês anterior.</span><span class="sxs-lookup"><span data-stu-id="a025b-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


